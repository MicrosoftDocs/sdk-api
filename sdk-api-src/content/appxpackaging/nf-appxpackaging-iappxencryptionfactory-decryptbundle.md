---
UID: NF:appxpackaging.IAppxEncryptionFactory.DecryptBundle
title: IAppxEncryptionFactory::DecryptBundle method
author: windows-driver-content
description: Creates an unencrypted Windows app bundle from an encrypted one.
old-location: appxpkg\iappxencryptionfactory_decryptbundle.htm
old-project: appxpkg
ms.assetid: ED10EBD7-F942-4F1D-B2DC-0895022771BE
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: DecryptBundle method [App packaging and management], DecryptBundle method [App packaging and management], IAppxEncryptionFactory interface, DecryptBundle,IAppxEncryptionFactory.DecryptBundle, IAppxEncryptionFactory, IAppxEncryptionFactory interface [App packaging and management], DecryptBundle method, IAppxEncryptionFactory::DecryptBundle, appxpackaging/IAppxEncryptionFactory::DecryptBundle, appxpkg.iappxencryptionfactory_decryptbundle
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
req.typenames: APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxEncryptionFactory.DecryptBundle
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxEncryptionFactory::DecryptBundle method


## -description


Creates an unencrypted Windows app bundle from an encrypted one.


## -parameters




### -param inputStream [in]

A readable stream from the app bundle to be decrypted.


### -param outputStream [in]

A writeable stream for writing the resulting decrypted app bundle.


### -param keyInfo [in]

Key info containing the base encryption key and key ID for decrypting the bundle. The base key is used to derive the per file encryption keys. If this parameter is null, the global test key and key ID are used.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/F07138FE-340F-4493-A3A9-AED075B2CEEA">IAppxEncryptionFactory</a>
 

 

