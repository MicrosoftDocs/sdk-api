---
UID: NF:appxpackaging.IAppxBundleManifestPackageInfoEnumerator.GetHasCurrent
title: IAppxBundleManifestPackageInfoEnumerator::GetHasCurrent
author: windows-driver-content
description: Determines whether there are more elements in the enumerator.
old-location: appxpkg\iappxbundlemanifestpackageinfoenumerator_gethascurrent.htm
old-project: appxpkg
ms.assetid: ED12F498-1F8D-45B2-9CFE-7215D2D87C3F
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetHasCurrent, GetHasCurrent method [App packaging and management], GetHasCurrent method [App packaging and management],IAppxBundleManifestPackageInfoEnumerator interface, IAppxBundleManifestPackageInfoEnumerator interface [App packaging and management],GetHasCurrent method, IAppxBundleManifestPackageInfoEnumerator.GetHasCurrent, IAppxBundleManifestPackageInfoEnumerator::GetHasCurrent, appxpackaging/IAppxBundleManifestPackageInfoEnumerator::GetHasCurrent, appxpkg.iappxbundlemanifestpackageinfoenumerator_gethascurrent
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
-	IAppxBundleManifestPackageInfoEnumerator.GetHasCurrent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxBundleManifestPackageInfoEnumerator::GetHasCurrent


## -description


Determines whether there are more elements in the enumerator.


## -parameters




### -param hasCurrent [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a>*</b>

<b>TRUE</b> if the enumerator's current position references an item; <b>FALSE</b> if the enumerator has passed the last item in the collection.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/4861D5CF-9FDC-4BAA-8462-D239DAEB5195">IAppxBundleManifestPackageInfoEnumerator</a>
 

 

