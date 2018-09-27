---
UID: NF:strmif.IAMTunerNotification.OnEvent
title: IAMTunerNotification::OnEvent
author: windows-sdk-content
description: Note  The IAMTunerNotification interface is deprecated. The OnEvent method handles events from the TV tuner card.
old-location: dshow\iamtunernotification_onevent.htm
tech.root: DirectShow
ms.assetid: ac28a445-dfa0-4e88-861d-3364106c2b20
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IAMTunerNotification interface [DirectShow],OnEvent method, IAMTunerNotification.OnEvent, IAMTunerNotification::OnEvent, IAMTunerNotificationOnEvent, OnEvent, OnEvent method [DirectShow], OnEvent method [DirectShow],IAMTunerNotification interface, dshow.iamtunernotification_onevent, strmif/IAMTunerNotification::OnEvent
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
 - IAMTunerNotification.OnEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMTunerNotification::OnEvent


## -description



<div class="alert"><b>Note</b>  The <b>IAMTunerNotification</b> interface is deprecated.</div>
<div> </div>
The <code>OnEvent</code> method handles events from the TV tuner card.




## -parameters




### -param Event [in]

Flag identifying the type of event. Currently, the only value defined is AMTUNER_EVENT_CHANGED.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/8e5fde62-d17c-4d3c-bdb0-0748a9bd285b">IAMTunerNotification Interface</a>
 

 

