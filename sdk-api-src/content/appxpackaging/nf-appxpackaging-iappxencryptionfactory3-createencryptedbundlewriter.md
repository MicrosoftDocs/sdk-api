---
UID: NF:appxpackaging.IAppxEncryptionFactory3.CreateEncryptedBundleWriter
title: IAppxEncryptionFactory3::CreateEncryptedBundleWriter
author: windows-sdk-content
description: Creates a write-only bundle object to which encrypted Windows app packages can be added.
old-location: appxpkg\iappxencryptionfactory3_createencryptedbundlewriter.htm
old-project: appxpkg
ms.assetid: 6E12E38B-23F3-437A-B3DF-1614663CFD3F
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: CreateEncryptedBundleWriter, CreateEncryptedBundleWriter method [App packaging and management], CreateEncryptedBundleWriter method [App packaging and management],IAppxEncryptionFactory3 interface, IAppxEncryptionFactory3 interface [App packaging and management],CreateEncryptedBundleWriter method, IAppxEncryptionFactory3.CreateEncryptedBundleWriter, IAppxEncryptionFactory3::CreateEncryptedBundleWriter, appxpackaging/IAppxEncryptionFactory3::CreateEncryptedBundleWriter, appxpkg.iappxencryptionfactory3_createencryptedbundlewriter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: appxpackaging.h
req.include-header: 
req.redist: 
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
 - IAppxEncryptionFactory3.CreateEncryptedBundleWriter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxEncryptionFactory3::CreateEncryptedBundleWriter


## -description


Creates a write-only bundle object to which encrypted Windows app packages can be added.  


## -parameters




### -param outputStream [in]

A writeable stream for writing the resulting encrypted app bundle.


### -param bundleVersion [in]

The version number of the bundle. If the bundle version is 0, a default version based on the current system time will be generated.


### -param settings [in]

Settings for creating the package.


### -param keyInfo [in]

Key info containing the base encryption key and key ID for decrypting the bundle. The base key is used to derive the per file encryption keys. If this parameter is null, the global test key and key ID are used.


### -param exemptedFiles [in]

Files exempted from the bundle writer.


### -param bundleWriter [out, retval]

The bundle writer object created.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ABF2F4BE-FC6A-4AF5-BD15-243ABFA055D9">IAppxEncryptionFactory3</a>
 

 

