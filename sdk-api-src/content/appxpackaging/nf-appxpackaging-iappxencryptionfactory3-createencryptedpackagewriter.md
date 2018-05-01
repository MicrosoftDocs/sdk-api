---
UID: NF:appxpackaging.IAppxEncryptionFactory3.CreateEncryptedPackageWriter
title: IAppxEncryptionFactory3::CreateEncryptedPackageWriter method
author: windows-driver-content
description: Creates a new instance of an IAppxEncryptedPackageWriter.
old-location: appxpkg\iappxencryptionfactory3_createencryptedpackagewriter.htm
old-project: appxpkg
ms.assetid: 9CBBAF89-DE9F-49B6-B03A-2F3B6B4CE1E4
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: CreateEncryptedPackageWriter method [App packaging and management], CreateEncryptedPackageWriter method [App packaging and management], IAppxEncryptionFactory3 interface, CreateEncryptedPackageWriter,IAppxEncryptionFactory3.CreateEncryptedPackageWriter, IAppxEncryptionFactory3, IAppxEncryptionFactory3 interface [App packaging and management], CreateEncryptedPackageWriter method, IAppxEncryptionFactory3::CreateEncryptedPackageWriter, appxpackaging/IAppxEncryptionFactory3::CreateEncryptedPackageWriter, appxpkg.iappxencryptionfactory3_createencryptedpackagewriter
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
req.typenames: APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxEncryptionFactory3.CreateEncryptedPackageWriter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxEncryptionFactory3::CreateEncryptedPackageWriter method


## -description


Creates a new instance of an <a href="https://msdn.microsoft.com/19096DFB-A8CF-4DEF-863B-3DBB9E893A8D">IAppxEncryptedPackageWriter</a>.


## -parameters




### -param outputStream [in]

A writeable stream for sending bytes produced by the app package.


### -param manifestStream [in]

A readable stream that defines the package for the  AppxManifest.xml.


### -param contentGroupMapStream [in]

A stream that defines the content group map.


### -param settings [in]

Settings for creating the package.


### -param keyInfo [in]

Key info containing the base encryption key and key ID for encrypting the package. The base encryption key is used to derive the per file encryption keys. If this parameter is null, the global test key and key ID are used.


### -param exemptedFiles [in]

Files exempted from the package writer.


### -param packageWriter [out, retval]

The package writer object created.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ABF2F4BE-FC6A-4AF5-BD15-243ABFA055D9">IAppxEncryptionFactory3</a>
 

 

