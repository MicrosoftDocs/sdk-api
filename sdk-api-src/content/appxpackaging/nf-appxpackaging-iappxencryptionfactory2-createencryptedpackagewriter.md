---
UID: NF:appxpackaging.IAppxEncryptionFactory2.CreateEncryptedPackageWriter
title: IAppxEncryptionFactory2::CreateEncryptedPackageWriter (appxpackaging.h)
description: Creates a new instance of an IAppxEncryptedPackageWriter. (IAppxEncryptionFactory2.CreateEncryptedPackageWriter)
helpviewer_keywords: ["CreateEncryptedPackageWriter","CreateEncryptedPackageWriter method [App packaging and management]","CreateEncryptedPackageWriter method [App packaging and management]","IAppxEncryptionFactory2 interface","IAppxEncryptionFactory2 interface [App packaging and management]","CreateEncryptedPackageWriter method","IAppxEncryptionFactory2.CreateEncryptedPackageWriter","IAppxEncryptionFactory2::CreateEncryptedPackageWriter","appxpackaging/IAppxEncryptionFactory2::CreateEncryptedPackageWriter","appxpkg.iappxencryptionfactory2_createencryptedpackagewriter"]
old-location: appxpkg\iappxencryptionfactory2_createencryptedpackagewriter.htm
tech.root: appxpkg
ms.assetid: 70C3B332-7FB5-49CD-B0E2-43FD44AFF813
ms.date: 12/05/2018
ms.keywords: CreateEncryptedPackageWriter, CreateEncryptedPackageWriter method [App packaging and management], CreateEncryptedPackageWriter method [App packaging and management],IAppxEncryptionFactory2 interface, IAppxEncryptionFactory2 interface [App packaging and management],CreateEncryptedPackageWriter method, IAppxEncryptionFactory2.CreateEncryptedPackageWriter, IAppxEncryptionFactory2::CreateEncryptedPackageWriter, appxpackaging/IAppxEncryptionFactory2::CreateEncryptedPackageWriter, appxpkg.iappxencryptionfactory2_createencryptedpackagewriter
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
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
 - IAppxEncryptionFactory2::CreateEncryptedPackageWriter
 - appxpackaging/IAppxEncryptionFactory2::CreateEncryptedPackageWriter
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
 - IAppxEncryptionFactory2.CreateEncryptedPackageWriter
---

# IAppxEncryptionFactory2::CreateEncryptedPackageWriter


## -description

Creates a new instance of an <a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxencryptedpackagewriter">IAppxEncryptedPackageWriter</a>.

## -parameters

### -param outputStream [in]

A writable stream for sending bytes produced by the app package.

### -param manifestStream [in]

A readable stream that defines the package for the  AppxManifest.xml.

### -param contentGroupMapStream [in]

A stream that defines the content group map.

### -param settings [in]

Settings for creating the package.

### -param keyInfo [in]

Key info containing the base encryption key and key ID for encrypting the package. The base encryption key is used to derive the per file encryption keys. If this parameter is null, the global test key and key ID are used.

### -param exemptedFiles [in]

Files exempted from the package writer.

### -param packageWriter [out, retval]

The package writer object created.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxencryptionfactory2">IAppxEncryptionFactory2</a>
