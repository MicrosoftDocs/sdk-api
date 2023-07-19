---
UID: NF:appxpackaging.IAppxBundleFactory2.CreateBundleReader2
tech.root: appxpkg
title: IAppxBundleFactory2::CreateBundleReader2
ms.date: 02/13/2023
targetos: Windows
description: Creates a read-only bundle object that reads its contents from an IStream object, with an optional parameter for specifying the expected digest for the bundle.
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
 - IAppxBundleFactory2::CreateBundleReader2
f1_keywords:
 - IAppxBundleFactory2::CreateBundleReader2
 - appxpackaging/IAppxBundleFactory2::CreateBundleReader2
dev_langs:
 - c++
helpviewer_keywords:
 - CreateBundleReader2
---

## -description

Creates a read-only bundle object that reads its contents from an [IStream](../objidl/nn-objidl-istream.md) object, with an optional parameter for specifying the expected digest for the bundle.

## -parameters

### -param inputStream [in]

The input stream that delivers the content of the package for reading. The stream must support [ISequentialStream::Read](../objidl/nf-objidl-isequentialstream-read.md), [IStream::Seek](../objidl/nf-objidl-istream-seek.md), and [IStream::Stat](../objidl/nf-objidl-istream-stat.md). If these methods fail, their error codes may be passed to and returned by this method.

### -param expectedDigest [in,optional]

An LPCWSTR containing the expected digest, a hashed representation of the bundle file.

### -param bundleReader [out]

The created bundle reader.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an error code that includes, but is not limited to, those in the following table. 

| Return code | Description |
|-------------|-------------|
| APPX_E_INTERLEAVING_NOT_ALLOWED | The ZIP file delivered by *inputStream8 is an interleaved OPC package. |
| APPX_E_RELATIONSHIPS_NOT_ALLOWED | The OPC package delivered by *inputStream* contains OPC package/part relationships. |
| APPX_E_MISSING_REQUIRED_FILE | The OPC package delivered by *inputStream* does not have a manifest, or a block map, or a signature file when a CI catalog is present. |
| APPX_E_INVALID_MANIFEST | The bundle manifest is not valid. |
| APPX_E_INVALID_MANIFEST | The bundle manifest is not valid. |
| APPX_E_DIGEST_MISMATCH | The digest for the object doesn't match the digest provided in *expectedDigest*. |

## -remarks

Get the digest string for the *expecteDigest* parameter by calling [IAppxDigestProvider::GetDigest](nf-appxpackaging-iappxdigestprovider-getdigest.md).

## -see-also

