---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

