---
UID: NF:appxpackaging.IAppxEncryptionFactory.DecryptBundle
title: IAppxEncryptionFactory::DecryptBundle (appxpackaging.h)
description: Creates an unencrypted Windows app bundle from an encrypted one.
helpviewer_keywords: ["DecryptBundle","DecryptBundle method [App packaging and management]","DecryptBundle method [App packaging and management]","IAppxEncryptionFactory interface","IAppxEncryptionFactory interface [App packaging and management]","DecryptBundle method","IAppxEncryptionFactory.DecryptBundle","IAppxEncryptionFactory::DecryptBundle","appxpackaging/IAppxEncryptionFactory::DecryptBundle","appxpkg.iappxencryptionfactory_decryptbundle"]
old-location: appxpkg\iappxencryptionfactory_decryptbundle.htm
tech.root: appxpkg
ms.assetid: ED10EBD7-F942-4F1D-B2DC-0895022771BE
ms.date: 12/05/2018
ms.keywords: DecryptBundle, DecryptBundle method [App packaging and management], DecryptBundle method [App packaging and management],IAppxEncryptionFactory interface, IAppxEncryptionFactory interface [App packaging and management],DecryptBundle method, IAppxEncryptionFactory.DecryptBundle, IAppxEncryptionFactory::DecryptBundle, appxpackaging/IAppxEncryptionFactory::DecryptBundle, appxpkg.iappxencryptionfactory_decryptbundle
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
 - IAppxEncryptionFactory::DecryptBundle
 - appxpackaging/IAppxEncryptionFactory::DecryptBundle
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
 - IAppxEncryptionFactory.DecryptBundle
---

# IAppxEncryptionFactory::DecryptBundle


## -description

Creates an unencrypted Windows app bundle from an encrypted one.

## -parameters

### -param inputStream [in]

A readable stream from the app bundle to be decrypted.

### -param outputStream [in]

A validation stream for writing the resulting decrypted app bundle.

### -param keyInfo [in]

Key info containing the base encryption key and key ID for decrypting the bundle. The base key is used to derive the per file encryption keys. If this parameter is null, the global test key and key ID are used.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxencryptionfactory">IAppxEncryptionFactory</a>