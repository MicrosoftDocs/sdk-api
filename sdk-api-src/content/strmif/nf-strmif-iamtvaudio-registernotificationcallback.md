---
UID: NF:strmif.IAMTVAudio.RegisterNotificationCallBack
title: IAMTVAudio::RegisterNotificationCallBack (strmif.h)
author: windows-sdk-content
description: The RegisterNotificationCallBack method enables an object that implements the IAMTunerNotification interface to receive event notifications when the tuner changes state.
old-location: dshow\iamtvaudio_registernotificationcallback.htm
tech.root: DirectShow
ms.assetid: dfd8d0b3-e90f-4f77-9a26-0a4db03041ee
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMTVAudio interface [DirectShow],RegisterNotificationCallBack method, IAMTVAudio.RegisterNotificationCallBack, IAMTVAudio::RegisterNotificationCallBack, IAMTVAudioRegisterNotificationCallBack, RegisterNotificationCallBack, RegisterNotificationCallBack method [DirectShow], RegisterNotificationCallBack method [DirectShow],IAMTVAudio interface, dshow.iamtvaudio_registernotificationcallback, strmif/IAMTVAudio::RegisterNotificationCallBack
ms.topic: method
f1_keywords: 
 - "strmif/IAMTVAudio.RegisterNotificationCallBack"
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMTVAudio.RegisterNotificationCallBack
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMTVAudio::RegisterNotificationCallBack


## -description



The <code>RegisterNotificationCallBack</code> method enables an object that implements the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamtunernotification">IAMTunerNotification</a> interface to receive event notifications when the tuner changes state.



This method is not implemented.


## -parameters




### -param pNotify [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamtunernotification">IAMTunerNotification</a> interface that will receive the event notifications.


### -param lEvents [in]

Flag indicating that an event has occurred.


## -returns



Returns E_NOTIMPL.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamtvaudio">IAMTVAudio Interface</a>
 

 

