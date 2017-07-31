# lkml
build and maintain as separate trees all different linux kernels

The idea here is to take the linux-3.0.y branch of the linux kernel and maintain separate kernel trees for every different tag.
This allows for rapid searching for when a feature was installed or changed without having to play git games.
This can get unnmanageably large (several hundred gigabytes), so make use of the fact that files don't change
often between releases and use hardlinks to reduce the actual number of duplicate files.
