---
UID: NF:appxpackaging.IAppxEncryptionFactory4.EncryptPackage
title: IAppxEncryptionFactory4::EncryptPackage method
author: windows-driver-content
description: Creates an encrypted Windows app package from an unencrypted one.
old-location: appxpkg\iappxencryptionfactory4_encryptpackage.htm
old-project: appxpkg
ms.assetid: 3C47D7AD-CAD9-4623-A404-5676C51B5390
ms.author: windowsdriverdev
ms.date: 3/30/2018
ms.keywords: EncryptPackage method [App packaging and management], EncryptPackage method [App packaging and management], IAppxEncryptionFactory4 interface, EncryptPackage,IAppxEncryptionFactory4.EncryptPackage, IAppxEncryptionFactory4, IAppxEncryptionFactory4 interface [App packaging and management], EncryptPackage method, IAppxEncryptionFactory4::EncryptPackage, appxpackaging/IAppxEncryptionFactory4::EncryptPackage, appxpkg.iappxencryptionfactory4_encryptpackage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: APPX_PACKAGE_ARCHITECTURE2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxEncryptionFactory4.EncryptPackage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxEncryptionFactory4::EncryptPackage method


## -description


Creates an encrypted Windows app package from an unencrypted one.


## -parameters




### -param inputStream [in]

A readable stream from the app bundle to encrypt.


### -param outputStream [in]

A writeable stream for writing the resulting encrypted app bundle.


### -param settings [in]

Settings for creating the bundle.


### -param keyInfo [in]

Key info containing the base encryption key and key ID for encrypting the bundle. The base encryption key is used to derive the per file encryption keys. If this parameter is null, the global test key and key ID are used.


### -param exemptedFiles [in]

Files exempted from the package writer.


### -param memoryLimit [in]

The memory limit in bytes.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/BEB6BD9B-C265-4C92-98AD-59344B5274D4">IAppxEncryptionFactory4</a>
 

 

