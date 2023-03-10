---
UID: NF:appxpackaging.IAppxEncryptionFactory.DecryptPackage
title: IAppxEncryptionFactory::DecryptPackage (appxpackaging.h)
description: Creates an unencrypted Windows app package from an encrypted one.
helpviewer_keywords: ["DecryptPackage","DecryptPackage method [App packaging and management]","DecryptPackage method [App packaging and management]","IAppxEncryptionFactory interface","IAppxEncryptionFactory interface [App packaging and management]","DecryptPackage method","IAppxEncryptionFactory.DecryptPackage","IAppxEncryptionFactory::DecryptPackage","appxpackaging/IAppxEncryptionFactory::DecryptPackage","appxpkg.iappxencryptionfactory_decryptpackage"]
old-location: appxpkg\iappxencryptionfactory_decryptpackage.htm
tech.root: appxpkg
ms.assetid: FB3BC989-F165-417A-963A-7B78B65930FA
ms.date: 12/05/2018
ms.keywords: DecryptPackage, DecryptPackage method [App packaging and management], DecryptPackage method [App packaging and management],IAppxEncryptionFactory interface, IAppxEncryptionFactory interface [App packaging and management],DecryptPackage method, IAppxEncryptionFactory.DecryptPackage, IAppxEncryptionFactory::DecryptPackage, appxpackaging/IAppxEncryptionFactory::DecryptPackage, appxpkg.iappxencryptionfactory_decryptpackage
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
 - IAppxEncryptionFactory::DecryptPackage
 - appxpackaging/IAppxEncryptionFactory::DecryptPackage
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
 - IAppxEncryptionFactory.DecryptPackage
---

# IAppxEncryptionFactory::DecryptPackage


## -description

Creates an unencrypted Windows app package from an encrypted one.

## -parameters

### -param inputStream [in]

A readable stream from the app package to be decrypted.

### -param outputStream [in]

A writable stream for writing the resulting decrypted app package.

### -param keyInfo [in]

Key info containing the base encryption key and key ID for decrypting the package. The base encryption key is used to derive the per file encryption keys. If this parameter is null, the global test key and key ID are used.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxencryptionfactory">IAppxEncryptionFactory</a>