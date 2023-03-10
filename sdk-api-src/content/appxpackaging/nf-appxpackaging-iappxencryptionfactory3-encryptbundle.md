---
UID: NF:appxpackaging.IAppxEncryptionFactory3.EncryptBundle
title: IAppxEncryptionFactory3::EncryptBundle (appxpackaging.h)
description: Creates an encrypted Windows app bundle from an unencrypted one. (IAppxEncryptionFactory3.EncryptBundle)
helpviewer_keywords: ["EncryptBundle","EncryptBundle method [App packaging and management]","EncryptBundle method [App packaging and management]","IAppxEncryptionFactory3 interface","IAppxEncryptionFactory3 interface [App packaging and management]","EncryptBundle method","IAppxEncryptionFactory3.EncryptBundle","IAppxEncryptionFactory3::EncryptBundle","appxpackaging/IAppxEncryptionFactory3::EncryptBundle","appxpkg.iappxencryptionfactory3_encryptbundle"]
old-location: appxpkg\iappxencryptionfactory3_encryptbundle.htm
tech.root: appxpkg
ms.assetid: 4ECF7227-08A1-4AEB-8545-420090131FB8
ms.date: 12/05/2018
ms.keywords: EncryptBundle, EncryptBundle method [App packaging and management], EncryptBundle method [App packaging and management],IAppxEncryptionFactory3 interface, IAppxEncryptionFactory3 interface [App packaging and management],EncryptBundle method, IAppxEncryptionFactory3.EncryptBundle, IAppxEncryptionFactory3::EncryptBundle, appxpackaging/IAppxEncryptionFactory3::EncryptBundle, appxpkg.iappxencryptionfactory3_encryptbundle
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
 - IAppxEncryptionFactory3::EncryptBundle
 - appxpackaging/IAppxEncryptionFactory3::EncryptBundle
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
 - IAppxEncryptionFactory3.EncryptBundle
---

# IAppxEncryptionFactory3::EncryptBundle


## -description

Creates an encrypted Windows app bundle from an unencrypted one.

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

Files exempted from the bundle writer.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxencryptionfactory3">IAppxEncryptionFactory3</a>
