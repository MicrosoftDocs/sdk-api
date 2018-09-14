---
UID: NF:appxpackaging.IAppxBundleManifestPackageInfo2.GetIsPackageReference
title: IAppxBundleManifestPackageInfo2::GetIsPackageReference
author: windows-sdk-content
description: Determines whether a package is stored inside an app bundle, or if it's a reference to a package.
old-location: appxpkg\iappxbundlemanifestpackageinfo2_getispackagereference.htm
tech.root: appxpkg
ms.assetid: 0EAE15E9-5B23-43F4-B4C6-D75EC8D8F281
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetIsPackageReference, GetIsPackageReference method [App packaging and management], GetIsPackageReference method [App packaging and management],IAppxBundleManifestPackageInfo2 interface, IAppxBundleManifestPackageInfo2 interface [App packaging and management],GetIsPackageReference method, IAppxBundleManifestPackageInfo2.GetIsPackageReference, IAppxBundleManifestPackageInfo2::GetIsPackageReference, appxpackaging/IAppxBundleManifestPackageInfo2::GetIsPackageReference, appxpkg.iappxbundlemanifestpackageinfo2_getispackagereference
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
 - IAppxBundleManifestPackageInfo2.GetIsPackageReference
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxBundleManifestPackageInfo2::GetIsPackageReference


## -description


Determines whether a package is stored inside an app bundle, or if it's a reference to a package.


## -parameters




### -param isPackageReference [out, retval]

True if the package in the bundle is a reference to a package; False if the package in the bundle is stored inside the app bundle.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/036CD1E1-F4D7-46B9-A287-2728BA45348A">IAppxBundleManifestPackageInfo2</a>
 

 

