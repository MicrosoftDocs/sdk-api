---
UID: NF:appxpackaging.IAppxBundleManifestPackageInfo.GetOffset
title: IAppxBundleManifestPackageInfo::GetOffset
author: windows-driver-content
description: Retrieves the offset of the package relative to the beginning of the bundle.
old-location: appxpkg\iappxbundlemanifestpackageinfo_getoffset.htm
old-project: appxpkg
ms.assetid: A55DB4B6-2EA0-4392-B05A-FEE091913573
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetOffset, GetOffset method [App packaging and management], GetOffset method [App packaging and management],IAppxBundleManifestPackageInfo interface, IAppxBundleManifestPackageInfo interface [App packaging and management],GetOffset method, IAppxBundleManifestPackageInfo.GetOffset, IAppxBundleManifestPackageInfo::GetOffset, appxpackaging/IAppxBundleManifestPackageInfo::GetOffset, appxpkg.iappxbundlemanifestpackageinfo_getoffset
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
-	IAppxBundleManifestPackageInfo.GetOffset
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxBundleManifestPackageInfo::GetOffset


## -description


Retrieves the offset of the package relative to the beginning of the bundle.


## -parameters




### -param offset [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a>*</b>

The offset of the package, in bytes.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/B9272875-E02A-4443-82B3-C64104E8291C">IAppxBundleManifestPackageInfo</a>
 

 

