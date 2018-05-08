---
UID: NF:appxpackaging.IAppxBundleManifestPackageInfo.GetPackageId
title: IAppxBundleManifestPackageInfo::GetPackageId
author: windows-driver-content
description: Retrieves an object that represents the identity of the app package.
old-location: appxpkg\iappxbundlemanifestpackageinfo_getpackageid.htm
old-project: appxpkg
ms.assetid: 5C7F52C3-AB72-4023-900B-53E3B5504213
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetPackageId, GetPackageId method [App packaging and management], GetPackageId method [App packaging and management],IAppxBundleManifestPackageInfo interface, IAppxBundleManifestPackageInfo interface [App packaging and management],GetPackageId method, IAppxBundleManifestPackageInfo.GetPackageId, IAppxBundleManifestPackageInfo::GetPackageId, appxpackaging/IAppxBundleManifestPackageInfo::GetPackageId, appxpkg.iappxbundlemanifestpackageinfo_getpackageid
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
-	IAppxBundleManifestPackageInfo.GetPackageId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxBundleManifestPackageInfo::GetPackageId


## -description


Retrieves an object that represents the identity of the app package.


## -parameters




### -param packageId [out, retval]

Type: <b><a href="https://msdn.microsoft.com/8665AC2B-4D06-4684-99B1-E22533CA04AA">IAppxManifestPackageId</a>**</b>

The package identifier.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> method when you have finished using the <i>packageId</i> object.




## -see-also




<a href="https://msdn.microsoft.com/B9272875-E02A-4443-82B3-C64104E8291C">IAppxBundleManifestPackageInfo</a>
 

 

