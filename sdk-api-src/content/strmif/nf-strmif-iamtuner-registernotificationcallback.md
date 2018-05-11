---
UID: NF:strmif.IAMTuner.RegisterNotificationCallBack
title: IAMTuner::RegisterNotificationCallBack
author: windows-driver-content
description: The RegisterNotificationCallBack method enables an object to receive event notifications when the tuner changes state.
old-location: dshow\iamtuner_registernotificationcallback.htm
old-project: DirectShow
ms.assetid: e169039f-bce7-495a-a40f-385fa3d3d2ab
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IAMTuner interface [DirectShow],RegisterNotificationCallBack method, IAMTuner.RegisterNotificationCallBack, IAMTuner::RegisterNotificationCallBack, IAMTunerRegisterNotificationCallBack, RegisterNotificationCallBack, RegisterNotificationCallBack method [DirectShow], RegisterNotificationCallBack method [DirectShow],IAMTuner interface, dshow.iamtuner_registernotificationcallback, strmif/IAMTuner::RegisterNotificationCallBack
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMTuner.RegisterNotificationCallBack
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMTuner::RegisterNotificationCallBack


## -description



The <code>RegisterNotificationCallBack</code> method enables an object to receive event notifications when the tuner changes state.



This method is not implemented.


## -parameters




### -param pNotify [in]

Pointer to the <a href="https://msdn.microsoft.com/8e5fde62-d17c-4d3c-bdb0-0748a9bd285b">IAMTunerNotification</a> interface that will receive the event notifications.


### -param lEvents [in]

Flag indicating that an event has occurred.


## -returns



Returns E_NOTIMPL.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/997d39c5-a1a5-4d2d-8704-9846f149712c">IAMTuner Interface</a>
 

 

