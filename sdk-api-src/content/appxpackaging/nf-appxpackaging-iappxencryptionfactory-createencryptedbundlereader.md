---
UID: NF:appxpackaging.IAppxEncryptionFactory.CreateEncryptedBundleReader
title: IAppxEncryptionFactory::CreateEncryptedBundleReader (appxpackaging.h)
description: Creates a read-only bundle object to which encrypted Windows app packages can be added.helpviewer_keywords: ["CreateEncryptedBundleReader","CreateEncryptedBundleReader method [App packaging and management]","CreateEncryptedBundleReader method [App packaging and management]","IAppxEncryptionFactory interface","IAppxEncryptionFactory interface [App packaging and management]","CreateEncryptedBundleReader method","IAppxEncryptionFactory.CreateEncryptedBundleReader","IAppxEncryptionFactory::CreateEncryptedBundleReader","appxpackaging/IAppxEncryptionFactory::CreateEncryptedBundleReader","appxpkg.iappxencryptionfactory_createencryptedbundlereader"]
old-location: appxpkg\iappxencryptionfactory_createencryptedbundlereader.htm
tech.root: appxpkg
ms.assetid: 1802E721-9320-4B05-9C38-6C3AC3FB413C
ms.date: 12/05/2018
ms.keywords: CreateEncryptedBundleReader, CreateEncryptedBundleReader method [App packaging and management], CreateEncryptedBundleReader method [App packaging and management],IAppxEncryptionFactory interface, IAppxEncryptionFactory interface [App packaging and management],CreateEncryptedBundleReader method, IAppxEncryptionFactory.CreateEncryptedBundleReader, IAppxEncryptionFactory::CreateEncryptedBundleReader, appxpackaging/IAppxEncryptionFactory::CreateEncryptedBundleReader, appxpkg.iappxencryptionfactory_createencryptedbundlereader
f1_keywords:
- appxpackaging/IAppxEncryptionFactory.CreateEncryptedBundleReader
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
- IAppxEncryptionFactory.CreateEncryptedBundleReader
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxencryptionfactory">IAppxEncryptionFactory</a>
 

 

