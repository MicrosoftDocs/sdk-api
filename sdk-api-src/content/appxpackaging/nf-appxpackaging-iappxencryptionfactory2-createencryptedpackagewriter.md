---
UID: NF:appxpackaging.IAppxEncryptionFactory2.CreateEncryptedPackageWriter
title: IAppxEncryptionFactory2::CreateEncryptedPackageWriter
author: windows-sdk-content
description: Creates a new instance of an IAppxEncryptedPackageWriter.
old-location: appxpkg\iappxencryptionfactory2_createencryptedpackagewriter.htm
old-project: appxpkg
ms.assetid: 70C3B332-7FB5-49CD-B0E2-43FD44AFF813
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: CreateEncryptedPackageWriter, CreateEncryptedPackageWriter method [App packaging and management], CreateEncryptedPackageWriter method [App packaging and management],IAppxEncryptionFactory2 interface, IAppxEncryptionFactory2 interface [App packaging and management],CreateEncryptedPackageWriter method, IAppxEncryptionFactory2.CreateEncryptedPackageWriter, IAppxEncryptionFactory2::CreateEncryptedPackageWriter, appxpackaging/IAppxEncryptionFactory2::CreateEncryptedPackageWriter, appxpkg.iappxencryptionfactory2_createencryptedpackagewriter
ms.prod: windows
ms.technology: windows-sdk
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
 - IAppxEncryptionFactory2.CreateEncryptedPackageWriter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxEncryptionFactory2::CreateEncryptedPackageWriter


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




<a href="https://msdn.microsoft.com/CEA749C5-1DD0-4207-83BA-905B8838A923">IAppxEncryptionFactory2</a>
 

 

