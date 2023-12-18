---
weight: 55333503
title: FVecReader
---
## FVecReader

Reads ivec files with random access, using the input to specify the record number.

- `long -> FVecReader(String: pathname) -> float[]`

- `long -> FVecReader(String: pathname, int: expectedDimensions, int: recordLimit) -> float[]`

## IVecReader

Reads ivec files with random access, using the input to specify the record number. This is used for testing with generated KNN test data which is uniform in dimensions and neighborhood size. While it is possible to specify different dimensioned vectors per record, this is not supported, since this function honors the pure-function behavior of other NB binding functions. This requires uniform record structure for random access.

- `long -> IVecReader(String: pathname) -> int[]`
  - *notes:* Read the ivec file, determining the record size from the first record.
@param pathname The location of the ivec file

  - *example:* `IvecReader('testfile.ivec')`
  - *Create a reader for int vectors, detecting the dimensions and dataset size automatically.*

- `long -> IVecReader(String: pathname, int: expectedDimensions, int: recordLimit) -> int[]`
  - *example:* `IvecReader('testfile.ivec', 46, 12)`
  - *Create a reader for int vectors, asserting 46 dimensions and limit total records to 12.*

