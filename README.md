# MPFC-ROIs
NIFTI files from the MPFC review paper

These files are obtained by comparing the following composite terms in Neurosynth:
- Social: `(social | mentalizing)`,
- Self: `self`,
- Emotion: `emotion*`,
- Value: `(value | reward | incentive)`,
- Mental time travel: `(episodic | future | past | retrieval | prospective | memory retrieval)`

In the [maps](https://github.com/MetaD/MPFC-ROIs/maps), the value at each voxel indicates how many of the other 4 terms the current term wins over by a posterior probability of at least 0.60. For example, in social_posterior>0.6_map.nii.gz, when a voxel has a value 4, the posterior probability of the social term (`social | mentalizing`) at this voxel is greater than 0.60 when compared with any of the other 4 terms; when a voxel has a value 3, the social term wins over 3 out of the 4 other terms at this voxel; etc.

The [masks](https://github.com/MetaD/MPFC-ROIs/masks) are binary masks based on the above maps. The voxels with 4.0 in maps are converted to 1 in masks, and everything else is converted to 0. Clusters of sizes smaller than 3 voxels are removed from these masks (i.e. converted to 0).

Please see the MPFC review paper for more details. This comparison can be done with [NeurosynthPlus](https://github.com/MetaD/neurosynthPlus).
