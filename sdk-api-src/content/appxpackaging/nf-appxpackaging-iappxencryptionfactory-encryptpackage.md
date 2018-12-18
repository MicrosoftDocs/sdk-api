---
UID: NF:appxpackaging.IAppxEncryptionFactory.EncryptPackage
title: IAppxEncryptionFactory::EncryptPackage
author: windows-sdk-content
description: Creates an encrypted Windows app package from an unencrypted one.
old-location: appxpkg\iappxencryptionfactory_encryptpackage.htm
tech.root: appxpkg
ms.assetid: 2C77A9F9-340C-4846-8EDA-26FAB7E53D60
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EncryptPackage, EncryptPackage method [App packaging and management], EncryptPackage method [App packaging and management],IAppxEncryptionFactory interface, IAppxEncryptionFactory interface [App packaging and management],EncryptPackage method, IAppxEncryptionFactory.EncryptPackage, IAppxEncryptionFactory::EncryptPackage, appxpackaging/IAppxEncryptionFactory::EncryptPackage, appxpkg.iappxencryptionfactory_encryptpackage
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

TBD




## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/F07138FE-340F-4493-A3A9-AED075B2CEEA">IAppxEncryptionFactory</a>
 

 

