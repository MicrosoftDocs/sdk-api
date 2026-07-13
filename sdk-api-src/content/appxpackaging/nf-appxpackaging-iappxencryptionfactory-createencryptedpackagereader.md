---
UID: NF:appxpackaging.IAppxEncryptionFactory.CreateEncryptedPackageReader
title: IAppxEncryptionFactory::CreateEncryptedPackageReader (appxpackaging.h)
description: Creates a new instance of IAppxPackageReader for reading encrypted packages.
helpviewer_keywords: ["CreateEncryptedPackageReader","CreateEncryptedPackageReader method [App packaging and management]","CreateEncryptedPackageReader method [App packaging and management]","IAppxEncryptionFactory interface","IAppxEncryptionFactory interface [App packaging and management]","CreateEncryptedPackageReader method","IAppxEncryptionFactory.CreateEncryptedPackageReader","IAppxEncryptionFactory::CreateEncryptedPackageReader","appxpackaging/IAppxEncryptionFactory::CreateEncryptedPackageReader","appxpkg.iappxencryptionfactory_createencryptedpackagereader"]
old-location: appxpkg\iappxencryptionfactory_createencryptedpackagereader.htm
tech.root: appxpkg
ms.assetid: 325E4883-69D7-4E2A-A664-3CA3C5559CB3
ms.date: 12/05/2018
ms.keywords: CreateEncryptedPackageReader, CreateEncryptedPackageReader method [App packaging and management], CreateEncryptedPackageReader method [App packaging and management],IAppxEncryptionFactory interface, IAppxEncryptionFactory interface [App packaging and management],CreateEncryptedPackageReader method, IAppxEncryptionFactory.CreateEncryptedPackageReader, IAppxEncryptionFactory::CreateEncryptedPackageReader, appxpackaging/IAppxEncryptionFactory::CreateEncryptedPackageReader, appxpkg.iappxencryptionfactory_createencryptedpackagereader
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: AppxPackaging.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAppxEncryptionFactory::CreateEncryptedPackageReader
 - appxpackaging/IAppxEncryptionFactory::CreateEncryptedPackageReader
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxEncryptionFactory.CreateEncryptedPackageReader
---

# IAppxEncryptionFactory::CreateEncryptedPackageReader


## -description

Creates a new instance of [IAppxPackageReader](nn-appxpackaging-iappxpackagereader.md) for reading encrypted packages.

## -parameters

### -param inputStream [in]

A readable stream from the app package.

### -param keyInfo [in]

Key info containing the base encryption key and key ID for encrypting the package. The base encryption key is used to derive the per file encryption keys. If this parameter is null, the global test key and key ID are used.

### -param packageReader [out, retval]

The package reader object created.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxencryptionfactory">IAppxEncryptionFactory</a>