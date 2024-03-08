---
UID: NF:appxpackaging.IAppxFactory3.CreatePackageReader2
tech.root: appxpkg
title: IAppxFactory3::CreatePackageReader2
ms.date: 02/13/2023
targetos: Windows
description: Creates a read-only package reader from the contents provided by an IStream, with an optional parameter for specifying the expected digest for the package.
prerelease: true
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: appxpackaging.h
req.idl: AppxPackaging.idl
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - appxpackaging.h
api_name:
 - IAppxFactory3::CreatePackageReader2
f1_keywords:
 - IAppxFactory3::CreatePackageReader2
 - appxpackaging/IAppxFactory3::CreatePackageReader2
dev_langs:
 - c++
helpviewer_keywords:
 - CreatePackageReader2
---

## -description

Creates a read-only package reader from the contents provided by an [IStream](../objidl/nn-objidl-istream.md), with an optional parameter for specifying the expected digest for the package. This method does not validate the digital signature.

## -parameters

### -param inputStream [in]

The input stream that delivers the package for reading. The stream must support [ISequentialStream::Read](../objidl/nf-objidl-isequentialstream-read.md), [IStream::Seek](../objidl/nf-objidl-istream-seek.md), and [IStream::Stat](../objidl/nf-objidl-istream-stat.md). If these methods fail, their error codes may be passed to and returned by this method.

### -param expectedDigest [in,optional]

An LPCWSTR containing the expected digest, a hashed representation of the package file.

### -param packageReader [out]

The created package reader.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an error code that includes, but is not limited to, those in the following table. 

| Return code | Description |
|-------------|-------------|
| APPX_E_INTERLEAVING_NOT_ALLOWED | The ZIP file delivered by *inputStream* is an interleaved OPC package.
| APPX_E_RELATIONSHIPS_NOT_ALLOWED | The OPC package delivered by <i>inputStream</i> contains OPC package/part relationships. |
| APPX_E_MISSING_REQUIRED_FILE | The OPC package delivered by <i>inputStream</i> does not have a manifest, or a block map, or a signature file when a CI catalog is present. |
| APPX_E_INVALID_MANIFEST | The package manifest is not valid. |
| APPX_E_INVALID_BLOCKMAP | The package block map is not valid, the list of files in the ZIP central directory does not match the list of files in the block map, or the size of files listed in the ZIP central directory does not match the file and block sizes listed in the block map. |
| APPX_E_DIGEST_MISMATCH | The digest for the object doesn't match the digest provided in *expectedDigest*. |

## -remarks

The  **CreatePackageReader2** method immediately retrieves footprint elements of the app package through the stream and validates their content.  This method succeeds only if the OPC package and all footprint elements (including ZIP central directory, manifest, [Content_Types].xml, and block map) are valid.  

Get the digest string for the *expecteDigest* parameter by calling [IAppxDigestProvider::GetDigest](nf-appxpackaging-iappxdigestprovider-getdigest.md).

#### Examples

For an example, see [Quickstart: Extract app package contents](/windows/desktop/appxpkg/how-to-extract-content-from-a-package)</a> and [Quickstart: Read app package manifest info](/windows/desktop/appxpkg/how-to-query-package-identity-information).

## -see-also

