---
UID: NF:appxpackaging.IAppxEncryptionFactory.EncryptBundle
title: IAppxEncryptionFactory::EncryptBundle (appxpackaging.h)
description: Creates an encrypted Windows app bundle from an unencrypted one.helpviewer_keywords: ["EncryptBundle","EncryptBundle method [App packaging and management]","EncryptBundle method [App packaging and management]","IAppxEncryptionFactory interface","IAppxEncryptionFactory interface [App packaging and management]","EncryptBundle method","IAppxEncryptionFactory.EncryptBundle","IAppxEncryptionFactory::EncryptBundle","appxpackaging/IAppxEncryptionFactory::EncryptBundle","appxpkg.iappxencryptionfactory_encryptbundle"]
old-location: appxpkg\iappxencryptionfactory_encryptbundle.htm
tech.root: appxpkg
ms.assetid: F2FFBB18-4E62-4704-B252-1749058A0A5E
ms.date: 12/05/2018
ms.keywords: EncryptBundle, EncryptBundle method [App packaging and management], EncryptBundle method [App packaging and management],IAppxEncryptionFactory interface, IAppxEncryptionFactory interface [App packaging and management],EncryptBundle method, IAppxEncryptionFactory.EncryptBundle, IAppxEncryptionFactory::EncryptBundle, appxpackaging/IAppxEncryptionFactory::EncryptBundle, appxpkg.iappxencryptionfactory_encryptbundle
f1_keywords:
- appxpackaging/IAppxEncryptionFactory.EncryptBundle
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
- IAppxEncryptionFactory.EncryptBundle
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxEncryptionFactory::EncryptBundle


## -description


Creates an encrypted Windows app bundle from an unencrypted one.


## -parameters




### -param inputStream [in]

A readable stream from the app bundle to encrypt.


### -param outputStream [in]

A writeable stream for writing the resulting encrypted app bundle.


### -param settings [in]

Settings for creating the bundle.


### -param keyInfo [in]

Key info containing the base encryption key and key ID for encrypting the bundle. The base encryption key is used to derive the per file encryption keys. If this parameter is null, the global test key and key ID are used.


### -param exemptedFiles

The list of files to be exempted from encryption.




## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxencryptionfactory">IAppxEncryptionFactory</a>
 

 

