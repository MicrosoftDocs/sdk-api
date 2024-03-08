---
UID: NF:appxpackaging.IAppxFactory3.CreateManifestReader2
tech.root: appxpkg
title: IAppxFactory3::CreateManifestReader2
ms.date: 02/13/2023
targetos: Windows
description: Creates a read-only manifest object model from contents provided by an IStream, with an optional parameter for specifying the expected digest for the manifest.
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
 - IAppxFactory3::CreateManifestReader2
f1_keywords:
 - IAppxFactory3::CreateManifestReader2
 - appxpackaging/IAppxFactory3::CreateManifestReader2
dev_langs:
 - c++
helpviewer_keywords:
 - CreateManifestReader2
---

## -description

Creates a read-only manifest object model from contents provided by an [IStream](../objidl/nn-objidl-istream.md), with an optional parameter for specifying the expected digest for the manifest.

## -parameters

### -param inputStream [in]

The input stream  that delivers the manifest XML for reading. The stream must support [ISequentialStream::Read](../objidl/nf-objidl-isequentialstream-read.md), [IStream::Seek](../objidl/nf-objidl-istream-seek.md), and [IStream::Stat](../objidl/nf-objidl-istream-stat.md). If these methods fail, their error codes may be passed to and returned by this method.

### -param expectedDigest [in,optional]

An LPCWSTR containing the expected digest, a hashed representation of the manifest file.

### -param manifestReader [out]

The created manifest reader.

## -returns

If the method succeeds, it returns **S_OK**. Otherwise, it returns an error code that includes, but is not limited to, those in the following table. 

| Return code | Description |
|-------------|-------------|
| APPX_E_INVALID_MANIFEST | The *inputStream* does not contain syntactically valid XML for the manifest. |
| APPX_E_DIGEST_MISMATCH | The digest for the object doesn't match the digest provided in *expectedDigest*. |

## -remarks

Use **CreateManifestReader2** to read a manifest outside of an app package. This method validates the manifest XML. The *manifestReader* provides access to all data elements and attributes in the manifest XML. The manifest logs the location of manifest validation errors in the ETW event log for AppxPackaging.

Get the digest string for the *expecteDigest* parameter by calling [IAppxDigestProvider::GetDigest](nf-appxpackaging-iappxdigestprovider-getdigest.md).

#### Examples

For an example, see [Quickstart: Read app package manifest info](/windows/desktop/appxpkg/how-to-query-package-identity-information).

## -see-also

