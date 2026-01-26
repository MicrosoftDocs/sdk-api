---
UID: NF:appxpackaging.IAppxFactory4.CreatePackageReaderFromSourceUri
tech.root: appxpkg
title: IAppxFactory4::CreatePackageReaderFromSourceUri
ms.date: 01/06/2026
targetos: Windows
description: Creates an instance of IAppxInstallerReader from the specified package location URI, with an optional parameter for specifying the expected digest for the App Installer file.
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
 - IAppxFactory4::CreatePackageReaderFromSourceUri
f1_keywords:
 - IAppxFactory4::CreatePackageReaderFromSourceUri
 - appxpackaging/IAppxFactory4::CreatePackageReaderFromSourceUri
dev_langs:
 - c++
helpviewer_keywords:
 - CreatePackageReaderFromSourceUri
---

## -description

Creates an instance of [IAppxPackageReader](nn-appxpackaging-iappxapppackagereader.md) from the specified package location URI, with an optional parameter for specifying the expected digest for the App Installer file.

## -parameters

### -param uri [in]

An LPCWSTR containing the URI of the package location.

### -param expectedDigest [in, optional]

An LPCWSTR containing the expected digest, a hashed representation of the App Installer File.

### -param packageReader [out]

Receives the created **IAppxPackageReader** instance.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an error code that includes, but is not limited to, those in the following table. 

| Return code | Description |
|-------------|-------------|
| APPX_E_DIGEST_MISMATCH | The digest for the object doesn't match the digest provided in *expectedDigest*. |
| APPX_E_MISSING_REQUIRED_FILE | The OPC package delivered by *uri* does not have a manifest, or a block map, or a signature file when a CI catalog is present. |
| E_POINTER | The *uri* or *bundleReader* param is NULL. |
| HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND) | The URI specified in *uri* is not valid. |

## -remarks

For HTTPS URIs, the server must support range requests.

## -see-also

