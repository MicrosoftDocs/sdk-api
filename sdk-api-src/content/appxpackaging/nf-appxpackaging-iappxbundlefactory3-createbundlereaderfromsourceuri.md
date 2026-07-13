---
UID: NF:appxpackaging.IAppxBundleFactory3.CreateBundleReaderFromSourceUri
tech.root: appxpkg
title: IAppxBundleFactory3::CreateBundleReaderFromSourceUri
ms.date: 01/06/2025
targetos: Windows
description: Creates a read-only bundle object that reads its contents from the specified URI, with an optional parameter for specifying the expected digest for the bundle.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: appxpackaging.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11 version 26100
req.target-min-winversvr: Windows Server 2025
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
 - IAppxBundleFactory3::CreateBundleReaderFromSourceUri
f1_keywords:
 - IAppxBundleFactory3::CreateBundleReaderFromSourceUri
 - appxpackaging/IAppxBundleFactory3::CreateBundleReaderFromSourceUri
dev_langs:
 - c++
helpviewer_keywords:
 - CreateBundleReaderFromSourceUri
---

## -description

Creates a read-only bundle object that reads its contents from the specified URI, with an optional parameter for specifying the expected digest for the bundle.

## -parameters

### -param uri [in]

An LPCWSTR containing the URI of the bundle location.

### -param expectedDigest [in, optional]

An LPCWSTR containing the expected digest, a hashed representation of the bundle file.

### -param bundleReader [out]

The created [IAppxBundleReader](nn-appxpackaging-iappxbundlereader.md) instance.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an error code that includes, but is not limited to, those in the following table. 

| Return code | Description |
|-------------|-------------|
| APPX_E_INTERLEAVING_NOT_ALLOWED | The ZIP file delivered by *uri* is an interleaved OPC package. |
| APPX_E_RELATIONSHIPS_NOT_ALLOWED | The OPC package delivered by *uri* contains OPC package/part relationships. |
| APPX_E_MISSING_REQUIRED_FILE | The OPC package delivered by *uri* does not have a manifest, or a block map, or a signature file when a CI catalog is present. |
| APPX_E_INVALID_MANIFEST | The bundle manifest is not valid. |
| APPX_E_DIGEST_MISMATCH | The digest for the object doesn't match the digest provided in *expectedDigest*. |
| E_POINTER | The *uri* or *bundleReader* param is NULL.|
| HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND) | The URI specified in *uri* is not valid. |

## -remarks

## -see-also

