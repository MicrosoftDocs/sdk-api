---
UID: NF:appxpackaging.IAppxEncryptionFactory.CreateEncryptedBundleReader
title: IAppxEncryptionFactory::CreateEncryptedBundleReader
author: windows-sdk-content
description: Creates a read-only bundle object to which encrypted Windows app packages can be added.
old-location: appxpkg\iappxencryptionfactory_createencryptedbundlereader.htm
old-project: appxpkg
ms.assetid: 1802E721-9320-4B05-9C38-6C3AC3FB413C
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: CreateEncryptedBundleReader, CreateEncryptedBundleReader method [App packaging and management], CreateEncryptedBundleReader method [App packaging and management],IAppxEncryptionFactory interface, IAppxEncryptionFactory interface [App packaging and management],CreateEncryptedBundleReader method, IAppxEncryptionFactory.CreateEncryptedBundleReader, IAppxEncryptionFactory::CreateEncryptedBundleReader, appxpackaging/IAppxEncryptionFactory::CreateEncryptedBundleReader, appxpkg.iappxencryptionfactory_createencryptedbundlereader
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxEncryptionFactory.CreateEncryptedBundleReader
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxEncryptionFactory::CreateEncryptedBundleReader


## -description


Creates a read-only bundle object to which encrypted Windows app packages can be added.


## -parameters




### -param inputStream [in]

A stream for reading the encrypted bundle.


### -param keyInfo [in]

 Key info containing the base encryption key and key ID for decrypting the bundle. The base key is used to derive the per file encryption keys. If this parameter is null, the global test key and key ID are used.


### -param bundleReader [out, retval]

The bundle reader object created.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/F07138FE-340F-4493-A3A9-AED075B2CEEA">IAppxEncryptionFactory</a>
 

 

