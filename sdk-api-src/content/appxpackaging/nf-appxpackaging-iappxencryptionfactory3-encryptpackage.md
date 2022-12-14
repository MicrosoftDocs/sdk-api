---
UID: NF:appxpackaging.IAppxEncryptionFactory3.EncryptPackage
title: IAppxEncryptionFactory3::EncryptPackage (appxpackaging.h)
description: Creates an encrypted Windows app package from an unencrypted one. (IAppxEncryptionFactory3.EncryptPackage)
helpviewer_keywords: ["EncryptPackage","EncryptPackage method [App packaging and management]","EncryptPackage method [App packaging and management]","IAppxEncryptionFactory3 interface","IAppxEncryptionFactory3 interface [App packaging and management]","EncryptPackage method","IAppxEncryptionFactory3.EncryptPackage","IAppxEncryptionFactory3::EncryptPackage","appxpackaging/IAppxEncryptionFactory3::EncryptPackage","appxpkg.iappxencryptionfactory3_encryptpackage"]
old-location: appxpkg\iappxencryptionfactory3_encryptpackage.htm
tech.root: appxpkg
ms.assetid: 2B3FE76E-57B5-411C-BD87-B9AE3208A11D
ms.date: 12/05/2018
ms.keywords: EncryptPackage, EncryptPackage method [App packaging and management], EncryptPackage method [App packaging and management],IAppxEncryptionFactory3 interface, IAppxEncryptionFactory3 interface [App packaging and management],EncryptPackage method, IAppxEncryptionFactory3.EncryptPackage, IAppxEncryptionFactory3::EncryptPackage, appxpackaging/IAppxEncryptionFactory3::EncryptPackage, appxpkg.iappxencryptionfactory3_encryptpackage
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
 - IAppxEncryptionFactory3::EncryptPackage
 - appxpackaging/IAppxEncryptionFactory3::EncryptPackage
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
 - IAppxEncryptionFactory3.EncryptPackage
---

# IAppxEncryptionFactory3::EncryptPackage


## -description

Creates an encrypted Windows app package from an unencrypted one.

## -parameters

### -param inputStream [in]

A readable stream from the app bundle to encrypt.

### -param outputStream [in]

A writable stream for writing the resulting encrypted app bundle.

### -param settings [in]

Settings for creating the bundle.

### -param keyInfo [in]

Key info containing the base encryption key and key ID for encrypting the bundle. The base encryption key is used to derive the per file encryption keys. If this parameter is null, the global test key and key ID are used.

### -param exemptedFiles [in]

Files exempted from the package writer.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxencryptionfactory3">IAppxEncryptionFactory3</a>
