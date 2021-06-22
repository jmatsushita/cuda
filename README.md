Haskell FFI Bindings to CUDA
============================

This fork builds Cuda on NixOS with an NVidia Titan XP graphics card.

[![Travis build status](https://img.shields.io/travis/tmcdonell/cuda/master.svg?label=linux)](https://travis-ci.org/tmcdonell/cuda)
[![AppVeyor build status](https://img.shields.io/appveyor/ci/tmcdonell/cuda/master.svg?label=windows)](https://ci.appveyor.com/project/tmcdonell/cuda)
[![Stackage LTS](https://stackage.org/package/cuda/badge/lts)](https://stackage.org/lts/package/cuda)
[![Stackage Nightly](https://stackage.org/package/cuda/badge/nightly)](https://stackage.org/nightly/package/cuda)
[![Hackage](https://img.shields.io/hackage/v/cuda.svg)](https://hackage.haskell.org/package/cuda)

The CUDA library provides a direct, general purpose C-like SPMD programming
model for NVIDIA graphics cards (G8x series onwards). This is a collection of
bindings to allow you to call and control, although not write, such functions
from Haskell-land. You will need to install the CUDA driver and developer
toolkit.

  <http://developer.nvidia.com/object/cuda.html>

The configure step will look for your CUDA installation in the standard places,
and if the `nvcc` compiler is found in your `PATH`, relative to that.

For important information on installing on Windows, see:

  <https://github.com/tmcdonell/cuda/blob/master/WINDOWS.md>


## Missing functionality

An incomplete list of missing bindings. Pull requests welcome!

### CUDA-9

- cuLaunchCooperativeKernelMultiDevice

### CUDA-10.0

- cuDeviceGetLuid (windows only?)
- cuLaunchHostFunc
- cuGraphHostNode[Get/Set]Params
- cuGraphKernelNode[Get/Set]Params
- cuGraphMemcpyNode[Get/Set]Params
- cuGraphMemsetNode[Get/Set]Params

### CUDA-10.2

- cuDeviceGetNvSciSyncAttributes
- cuMemAddressFree
- cuMemAddressReserve
- cuMemCreate
- cuMemExportToShareableHandle
- cuMemGetAccess
- cuMemGetAllocationGranularity
- cuMemGetAllocationPrepertiesFromHandle
- cuMemImportFromShareableHandle
- cuMemMap
- cuMemRelease
- cuMemSetAccess
- cuMemUnmap
- cuGraphExecHostNodeSetParams
- cuGraphExecMemcpyNodeSetParams
- cuGraphExecMemsetNodeSetParams
- cuGraphExecUpdate

