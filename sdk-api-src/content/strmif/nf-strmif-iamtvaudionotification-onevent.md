---
UID: NF:strmif.IAMTVAudioNotification.OnEvent
title: IAMTVAudioNotification::OnEvent
author: windows-sdk-content
description: Note  The IAMTVAudioNotification interface is deprecated. The OnEvent method handles events from a TV tuner card controlled by the IAMTVAudio interface.
old-location: dshow\iamtvaudionotification_onevent.htm
tech.root: DirectShow
ms.assetid: 5282cbbf-5501-42eb-95ba-bf7b32792d56
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAMTVAudioNotification interface [DirectShow],OnEvent method, IAMTVAudioNotification.OnEvent, IAMTVAudioNotification::OnEvent, IAMTVAudioNotificationOnEvent, OnEvent, OnEvent method [DirectShow], OnEvent method [DirectShow],IAMTVAudioNotification interface, dshow.iamtvaudionotification_onevent, strmif/IAMTVAudioNotification::OnEvent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
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
 - Strmif.h
api_name:
 - IAMTVAudioNotification.OnEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMTVAudioNotification::OnEvent


## -description



<div class="alert"><b>Note</b>  The <b>IAMTVAudioNotification</b> interface is deprecated.</div>
<div> </div>
The <code>OnEvent</code> method handles events from a TV tuner card controlled by the <a href="https://msdn.microsoft.com/de340594-4410-4896-b206-0f47d4035bc1">IAMTVAudio</a> interface.




## -parameters




### -param Event [in]

Flag identifying the type of event. The only value currently defined is AMTVAUDIO_EVENT_CHANGED.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/4f84586f-7384-4dd7-99ce-325fb609daae">IAMTVAudioNotification Interface</a>
 

 

