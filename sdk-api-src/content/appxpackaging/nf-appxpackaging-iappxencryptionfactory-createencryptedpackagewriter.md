---
UID: NF:appxpackaging.IAppxEncryptionFactory.CreateEncryptedPackageWriter
title: IAppxEncryptionFactory::CreateEncryptedPackageWriter (appxpackaging.h)
description: Creates a new instance of an IAppxEncryptedPackageWriter. (IAppxEncryptionFactory.CreateEncryptedPackageWriter)
helpviewer_keywords: ["CreateEncryptedPackageWriter","CreateEncryptedPackageWriter method [App packaging and management]","CreateEncryptedPackageWriter method [App packaging and management]","IAppxEncryptionFactory interface","IAppxEncryptionFactory interface [App packaging and management]","CreateEncryptedPackageWriter method","IAppxEncryptionFactory.CreateEncryptedPackageWriter","IAppxEncryptionFactory::CreateEncryptedPackageWriter","appxpackaging/IAppxEncryptionFactory::CreateEncryptedPackageWriter","appxpkg.iappxencryptionfactory_createencryptedpackagewriter"]
old-location: appxpkg\iappxencryptionfactory_createencryptedpackagewriter.htm
tech.root: appxpkg
ms.assetid: 01447B17-E197-4E08-B878-F5487F3E9E92
ms.date: 12/05/2018
ms.keywords: CreateEncryptedPackageWriter, CreateEncryptedPackageWriter method [App packaging and management], CreateEncryptedPackageWriter method [App packaging and management],IAppxEncryptionFactory interface, IAppxEncryptionFactory interface [App packaging and management],CreateEncryptedPackageWriter method, IAppxEncryptionFactory.CreateEncryptedPackageWriter, IAppxEncryptionFactory::CreateEncryptedPackageWriter, appxpackaging/IAppxEncryptionFactory::CreateEncryptedPackageWriter, appxpkg.iappxencryptionfactory_createencryptedpackagewriter
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
 - IAppxEncryptionFactory::CreateEncryptedPackageWriter
 - appxpackaging/IAppxEncryptionFactory::CreateEncryptedPackageWriter
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
 - IAppxEncryptionFactory.CreateEncryptedPackageWriter
---

# IAppxEncryptionFactory::CreateEncryptedPackageWriter


## -description

Creates a new instance of an <a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxencryptedpackagewriter">IAppxEncryptedPackageWriter</a>.

## -parameters

### -param outputStream [in]

A writable stream for sending bytes produced by the app package.

### -param manifestStream [in]

A readable stream that defines the package for the  AppxManifest.xml.

### -param settings [in]

Settings for creating the package.

### -param keyInfo [in]

Key info containing the base encryption key and key ID for encrypting the package. The base encryption key is used to derive the per file encryption keys. If this parameter is null, the global test key and key ID are used.

### -param exemptedFiles

The list of files to be exempted from encryption.

### -param packageWriter [out, retval]

The package writer object created.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxencryptionfactory">IAppxEncryptionFactory</a>
