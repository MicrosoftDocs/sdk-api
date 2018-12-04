---
UID: NF:appxpackaging.IAppxBundleManifestOptionalBundleInfoEnumerator.GetHasCurrent
title: IAppxBundleManifestOptionalBundleInfoEnumerator::GetHasCurrent
author: windows-sdk-content
description: Determines whether there is optional bundle information at the current position of the enumerator.
old-location: appxpkg\iappxbundlemanifestoptionalbundleinfoenumerator_gethascurrent.htm
tech.root: appxpkg
ms.assetid: C7473291-89EA-4412-848E-07257C0AC0FB
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetHasCurrent, GetHasCurrent method [App packaging and management], GetHasCurrent method [App packaging and management],IAppxBundleManifestOptionalBundleInfoEnumerator interface, IAppxBundleManifestOptionalBundleInfoEnumerator interface [App packaging and management],GetHasCurrent method, IAppxBundleManifestOptionalBundleInfoEnumerator.GetHasCurrent, IAppxBundleManifestOptionalBundleInfoEnumerator::GetHasCurrent, appxpackaging/IAppxBundleManifestOptionalBundleInfoEnumerator::GetHasCurrent, appxpkg.iappxbundlemanifestoptionalbundleinfoenumerator_gethascurrent
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
 - IAppxBundleManifestOptionalBundleInfoEnumerator.GetHasCurrent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxBundleManifestOptionalBundleInfoEnumerator::GetHasCurrent


## -description


Determines whether there is optional bundle information at the current position of the enumerator.


## -parameters




### -param hasCurrent [out, retval]

<b>TRUE</b> if the enumerator's current position references an item; <b>FALSE</b> if the enumerator has passed the last item in the collection.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5BF38EC7-7C04-455B-AFAA-CC2A78E54A4F">IAppxBundleManifestOptionalBundleInfoEnumerator</a>
 

 

