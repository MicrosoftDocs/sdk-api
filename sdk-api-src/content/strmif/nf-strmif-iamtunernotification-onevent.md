---
UID: NF:strmif.IAMTunerNotification.OnEvent
title: IAMTunerNotification::OnEvent (strmif.h)
author: windows-sdk-content
description: Note  The IAMTunerNotification interface is deprecated. The OnEvent method handles events from the TV tuner card.
old-location: dshow\iamtunernotification_onevent.htm
tech.root: DirectShow
ms.assetid: ac28a445-dfa0-4e88-861d-3364106c2b20
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMTunerNotification interface [DirectShow],OnEvent method, IAMTunerNotification.OnEvent, IAMTunerNotification::OnEvent, IAMTunerNotificationOnEvent, OnEvent, OnEvent method [DirectShow], OnEvent method [DirectShow],IAMTunerNotification interface, dshow.iamtunernotification_onevent, strmif/IAMTunerNotification::OnEvent
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
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamtunernotification">IAMTunerNotification Interface</a>
 

 

