---
UID: NF:tuner.IESRequestTunerEvent.GetEstimatedTime
title: IESRequestTunerEvent::GetEstimatedTime method
author: windows-driver-content
description: Gets a value indicating the amount of time that a device estimates it needs exclusive access to a tuner and its Conditional Access Services (CAS).
old-location: mstv\iesrequesttunerevent_getestimatedtime.htm
old-project: mstv
ms.assetid: 9968c1b1-5a4d-45a1-a083-afdbcc616f6d
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetEstimatedTime method [Microsoft TV Technologies], GetEstimatedTime method [Microsoft TV Technologies], IESRequestTunerEvent interface, GetEstimatedTime,IESRequestTunerEvent.GetEstimatedTime, IESRequestTunerEvent, IESRequestTunerEvent interface [Microsoft TV Technologies], GetEstimatedTime method, IESRequestTunerEvent::GetEstimatedTime, mstv.iesrequesttunerevent_getestimatedtime, tuner/IESRequestTunerEvent::GetEstimatedTime
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IESRequestTunerEvent.GetEstimatedTime
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IESRequestTunerEvent::GetEstimatedTime method


## -description



      Gets a value indicating the amount of time that a device estimates it  needs exclusive access to a tuner and its Conditional Access Services (CAS).


## -parameters




### -param pdwEstimatedTime [out, retval]


            Gets the estimated time that exclusive access is needed, in seconds.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/da1183a3-6f31-402a-b103-448cf13705a9">IESRequestTunerEvent</a>
 

 

