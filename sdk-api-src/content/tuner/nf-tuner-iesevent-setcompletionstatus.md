---
UID: NF:tuner.IESEvent.SetCompletionStatus
title: IESEvent::SetCompletionStatus method
author: windows-driver-content
description: Sets the completion status for an event that is derived from the IESEvent interface.
old-location: mstv\iesevent_setcompletionstatus.htm
old-project: mstv
ms.assetid: 2e8d5a94-6fa1-453b-bbd4-396d60bb2aa0
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IESEvent, IESEvent interface [Microsoft TV Technologies], SetCompletionStatus method, IESEvent::SetCompletionStatus, SetCompletionStatus method [Microsoft TV Technologies], SetCompletionStatus method [Microsoft TV Technologies], IESEvent interface, SetCompletionStatus,IESEvent.SetCompletionStatus, mstv.iesevent_setcompletionstatus, tuner/IESEvent::SetCompletionStatus
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
-	IESEvent.SetCompletionStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IESEvent::SetCompletionStatus method


## -description



      Sets the completion status for an event that is derived from the <a href="https://msdn.microsoft.com/3c375480-c6df-4bb0-b417-5765b0bed9bf">IESEvent</a> interface. The device handling the event sets the completion status in the <b>IESEvent</b> object that is passed in a call to <a href="https://msdn.microsoft.com/3781e50c-ab19-4bfa-86d6-af12223019ca">IESEventService::FireESEvent</a>.
    

If an event originates from a PBDA device, the event object automatically calls the <a href="https://msdn.microsoft.com/399530a7-5a02-485e-aa5e-6b3ddb7f3d54">IBDA_EventingService::CompleteEvent</a> method with the result set in the <b>SetCompletionStatus</b> call at the time it is released.  If the client is a managed application, it should dispose of the event object immediately after it is finished with the event. This disposition ensures that the <b>IBDA_EventingService::CompleteEvent</b> method is called in a timely manner


## -parameters




### -param dwResult [in]


            Completion status for the event.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3781e50c-ab19-4bfa-86d6-af12223019ca">FireESEvent</a>



<a href="https://msdn.microsoft.com/3c375480-c6df-4bb0-b417-5765b0bed9bf">IESEvent</a>
 

 

