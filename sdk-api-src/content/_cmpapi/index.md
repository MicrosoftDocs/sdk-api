---
UID: TP:cmpapi
ms.assetid: 865b4105-cb5f-37f2-b782-91e1abe4269c
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
---

# Compression API

## -description

Overview of the Compression API technology.

To develop Compression API, you need these headers:

 * [compressapi.h](../compressapi/index.md)

For the programming guide, see [Compression API](/windows/desktop/cmpapi).

## Functions

| Title   | Description   |
| ---- |:---- |
| [CloseCompressor function](..\compressapi\nf-compressapi-closecompressor.md) | Call to close an open COMPRESSOR_HANDLE. |
| [CloseDecompressor function](..\compressapi\nf-compressapi-closedecompressor.md) | Call to close an open DECOMPRESSOR_HANDLE. |
| [Compress function](..\compressapi\nf-compressapi-compress.md) | Takes a block of information and compresses it. |
| [CreateCompressor function](..\compressapi\nf-compressapi-createcompressor.md) | Generates a new COMPRESSOR_HANDLE. |
| [CreateDecompressor function](..\compressapi\nf-compressapi-createdecompressor.md) | Generates a new DECOMPRESSOR_HANDLE. |
| [Decompress function](..\compressapi\nf-compressapi-decompress.md) | Takes a block of compressed information and decompresses it. |
| [QueryCompressorInformation function](..\compressapi\nf-compressapi-querycompressorinformation.md) | Queries a compressor for information for a particular compression algorithm. |
| [QueryDecompressorInformation function](..\compressapi\nf-compressapi-querydecompressorinformation.md) | Use this function to query information about a particular compression algorithm. |
| [ResetCompressor function](..\compressapi\nf-compressapi-resetcompressor.md) | Prepares the compressor for the compression of a new stream. |
| [ResetDecompressor function](..\compressapi\nf-compressapi-resetdecompressor.md) | Prepares the decompressor for the decompression of a new stream. |
| [SetCompressorInformation function](..\compressapi\nf-compressapi-setcompressorinformation.md) | Sets information in a compressor for a particular compression algorithm. |
| [SetDecompressorInformation function](..\compressapi\nf-compressapi-setdecompressorinformation.md) | Sets information in a decompressor for a particular compression algorithm. |

## Structures

| Title   | Description   |
| ---- |:---- |
| [_COMPRESS_ALLOCATION_ROUTINES structure](..\compressapi\ns-compressapi-_compress_allocation_routines.md) | A structure containing optional memory allocation and deallocation routines. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [COMPRESS_INFORMATION_CLASS enumeration](..\compressapi\ne-compressapi-compress_information_class.md) | The values of this enumeration identify the type of information class being set or retrieved. |
