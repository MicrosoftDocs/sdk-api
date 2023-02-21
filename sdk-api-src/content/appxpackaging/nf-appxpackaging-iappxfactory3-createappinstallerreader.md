---
UID: NF:appxpackaging.IAppxFactory3.CreateAppInstallerReader
tech.root: appxpkg
title: IAppxFactory3::CreateAppInstallerReader
ms.date: 02/10/2023
targetos: Windows
description: Creates an instance of IAppInstallerReader, with an optional parameter for specifying the expected digest for the App Installer file.
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
 - IAppxFactory3::CreateAppInstallerReader
f1_keywords:
 - IAppxFactory3::CreateAppInstallerReader
 - appxpackaging/IAppxFactory3::CreateAppInstallerReader
dev_langs:
 - c++
helpviewer_keywords:
 - CreateAppInstallerReader
---

## -description

Creates an instance of [IAppInstallerReader](nf-appxpackaging-iappxfactory3-createappinstallerreader.md), with an optional parameter for specifying the expected digest for the App Installer file.

## -parameters

### -param inputStream [in]

An [IStream](../objidl/nn-objidl-istream.md) that provides the contents of an App Installer File.

### -param expectedDigest [in, optional]

An LPCWSTR containing the expected digest, a hashed representation of the App Installer File.

### -param appInstallerReader [out]

Receives the created **IAppInstallerReader** Instance.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an error code that includes, but is not limited to, those in the following table. 

| Return code | Description |
|-------------|-------------|
| APPX_E_DIGEST_MISMATCH | The digest for the object doesn't match the digest provided in *expectedDigest*. |

## -remarks

Get the digest string for the *expecteDigest* parameter by calling [IAppxDigestProvider::GetDigest](nf-appxpackaging-iappxdigestprovider-getdigest.md).

## -see-also

[App Installer File overview](/windows/msix/app-installer/app-installer-file-overview)

