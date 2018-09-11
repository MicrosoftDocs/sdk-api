---
UID: NF:appxpackaging.IAppxEncryptionFactory.CreateEncryptedPackageReader
title: IAppxEncryptionFactory::CreateEncryptedPackageReader
author: windows-sdk-content
description: Creates a new instance of IAppxEncryptedPackageReader.
old-location: appxpkg\iappxencryptionfactory_createencryptedpackagereader.htm
tech.root: appxpkg
ms.assetid: 325E4883-69D7-4E2A-A664-3CA3C5559CB3
ms.author: windowssdkdev
ms.date: 08/16/2018
ms.keywords: CreateEncryptedPackageReader, CreateEncryptedPackageReader method [App packaging and management], CreateEncryptedPackageReader method [App packaging and management],IAppxEncryptionFactory interface, IAppxEncryptionFactory interface [App packaging and management],CreateEncryptedPackageReader method, IAppxEncryptionFactory.CreateEncryptedPackageReader, IAppxEncryptionFactory::CreateEncryptedPackageReader, appxpackaging/IAppxEncryptionFactory::CreateEncryptedPackageReader, appxpkg.iappxencryptionfactory_createencryptedpackagereader
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IAppxEncryptionFactory.CreateEncryptedPackageReader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxEncryptionFactory::CreateEncryptedPackageReader


## -description


Creates a new instance of <a href="appxpkg.iappxencryptedpackagereader">IAppxEncryptedPackageReader</a>.


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




<a href="https://msdn.microsoft.com/F07138FE-340F-4493-A3A9-AED075B2CEEA">IAppxEncryptionFactory</a>
 

 

