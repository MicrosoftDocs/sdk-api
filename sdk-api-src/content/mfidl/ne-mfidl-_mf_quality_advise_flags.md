---
UID: NE:mfidl._MF_QUALITY_ADVISE_FLAGS
title: "_MF_QUALITY_ADVISE_FLAGS"
author: windows-sdk-content
description: Contains flags for the IMFQualityAdvise2::NotifyQualityEvent method.
old-location: mf\mf_quality_advise_flags.htm
tech.root: medfound
ms.assetid: 93cf5585-fcb4-480a-b482-241376e8ec73
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: MF_QUALITY_ADVISE_FLAGS, MF_QUALITY_ADVISE_FLAGS enumeration [Media Foundation], MF_QUALITY_CANNOT_KEEP_UP, _MF_QUALITY_ADVISE_FLAGS, mf.mf_quality_advise_flags, mfidl/MF_QUALITY_ADVISE_FLAGS, mfidl/MF_QUALITY_CANNOT_KEEP_UP
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MF_QUALITY_ADVISE_FLAGS
product: Windows
targetos: Windows
req.typenames: MF_QUALITY_ADVISE_FLAGS
req.redist: 
---

# _MF_QUALITY_ADVISE_FLAGS enumeration


## -description


Contains flags for the <a href="https://msdn.microsoft.com/7e39d421-1e7c-4b6d-beba-e24429271378">IMFQualityAdvise2::NotifyQualityEvent</a> method.


## -enum-fields




### -field MF_QUALITY_CANNOT_KEEP_UP

The decoder has done everything that it can to reduce sample latency, and samples are still late.


## -remarks



If the decoder sets the <b>MF_QUALITY_CANNOT_KEEP_UP</b> flag, the quality manager tries to reduce latency through the media source and the media sink. For example, it might request the <a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a> (EVR) to drop frames. During this period, the quality manager stops calling the decoder's <a href="https://msdn.microsoft.com/7e39d421-1e7c-4b6d-beba-e24429271378">IMFQualityAdvise2::NotifyQualityEvent</a> method, until samples are no longer arriving late at the sink. At that point, the quality manager resumes calling <b>NotifyQualityEvent</b> on the decoder.




## -see-also




<a href="https://msdn.microsoft.com/c6114bbc-31d8-45eb-9bf8-745b3138dd50">IMFQualityAdvise2</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

