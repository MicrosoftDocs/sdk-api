---
UID: NF:amstream.IAMMediaTypeSample.SetMediaTime
title: IAMMediaTypeSample::SetMediaTime
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. The SetMediaTime method sets the media time stamps for this sample.
old-location: dshow\iammediatypesample_setmediatime.htm
tech.root: DirectShow
ms.assetid: d255840f-9ff5-4eb0-b3b4-1295d77403f8
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IAMMediaTypeSample interface [DirectShow],SetMediaTime method, IAMMediaTypeSample.SetMediaTime, IAMMediaTypeSample::SetMediaTime, IAMMediaTypeSampleSetMediaTime, SetMediaTime, SetMediaTime method [DirectShow], SetMediaTime method [DirectShow],IAMMediaTypeSample interface, amstream/IAMMediaTypeSample::SetMediaTime, dshow.iammediatypesample_setmediatime
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: amstream.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - amstream.h
api_name:
 - IAMMediaTypeSample.SetMediaTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMMediaTypeSample::SetMediaTime


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>SetMediaTime</code> method sets the media time stamps for this sample.




## -parameters




### -param pTimeStart [in]

Pointer to a variable that contains the media start time.


### -param pTimeEnd [in]

Pointer to a variable that contains the media stop time.


## -returns



Returns S_OK.




## -see-also




<a href="https://msdn.microsoft.com/e0a62251-68ee-4318-b09a-0aac6b73bf54">IAMMediaTypeSample Interface</a>
 

 

