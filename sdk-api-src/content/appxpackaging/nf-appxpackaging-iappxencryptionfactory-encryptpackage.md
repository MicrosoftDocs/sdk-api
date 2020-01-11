---
UID: NF:appxpackaging.IAppxEncryptionFactory.EncryptPackage
title: IAppxEncryptionFactory::EncryptPackage (appxpackaging.h)
description: Creates an encrypted Windows app package from an unencrypted one.
old-location: appxpkg\iappxencryptionfactory_encryptpackage.htm
tech.root: appxpkg
ms.assetid: 2C77A9F9-340C-4846-8EDA-26FAB7E53D60
ms.date: 12/05/2018
ms.keywords: EncryptPackage, EncryptPackage method [App packaging and management], EncryptPackage method [App packaging and management],IAppxEncryptionFactory interface, IAppxEncryptionFactory interface [App packaging and management],EncryptPackage method, IAppxEncryptionFactory.EncryptPackage, IAppxEncryptionFactory::EncryptPackage, appxpackaging/IAppxEncryptionFactory::EncryptPackage, appxpkg.iappxencryptionfactory_encryptpackage
f1_keywords:
- appxpackaging/IAppxEncryptionFactory.EncryptPackage
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- AppxPackaging.h
api_name:
- IAppxEncryptionFactory.EncryptPackage
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxEncryptionFactory::EncryptPackage


## -description


Creates an encrypted Windows app package from an unencrypted one.


## -parameters




### -param inputStream [in]

A readable stream from the app package to be encrypted.


### -param outputStream [in]

A writeable stream for writing the resulting encrypted app package.


### -param settings [in]

Settings for creating the package.


### -param keyInfo [in]

Key information containing the base encryption key and key ID. The base key is used to derive the per file encryption keys. If the base key is null, the global test key and key Id are used.


### -param exemptedFiles

The list of files to be exempted from encryption.




## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxencryptionfactory">IAppxEncryptionFactory</a>
 

 

