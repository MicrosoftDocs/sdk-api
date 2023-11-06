---
UID: NF:tuner.IESEvent.SetCompletionStatus
title: IESEvent::SetCompletionStatus (tuner.h)
description: Sets the completion status for an event that is derived from the IESEvent interface.
helpviewer_keywords: ["IESEvent interface [Microsoft TV Technologies]","SetCompletionStatus method","IESEvent.SetCompletionStatus","IESEvent::SetCompletionStatus","SetCompletionStatus","SetCompletionStatus method [Microsoft TV Technologies]","SetCompletionStatus method [Microsoft TV Technologies]","IESEvent interface","mstv.iesevent_setcompletionstatus","tuner/IESEvent::SetCompletionStatus"]
old-location: mstv\iesevent_setcompletionstatus.htm
tech.root: mstv
ms.assetid: 2e8d5a94-6fa1-453b-bbd4-396d60bb2aa0
ms.date: 12/05/2018
ms.keywords: IESEvent interface [Microsoft TV Technologies],SetCompletionStatus method, IESEvent.SetCompletionStatus, IESEvent::SetCompletionStatus, SetCompletionStatus, SetCompletionStatus method [Microsoft TV Technologies], SetCompletionStatus method [Microsoft TV Technologies],IESEvent interface, mstv.iesevent_setcompletionstatus, tuner/IESEvent::SetCompletionStatus
f1_keywords:
- tuner/IESEvent.SetCompletionStatus
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- tuner.h
api_name:
- IESEvent.SetCompletionStatus
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IESEvent::SetCompletionStatus


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]


Sets the completion status for an event that is derived from the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesevent">IESEvent</a> interface. The device handling the event sets the completion status in the <b>IESEvent</b> object that is passed in a call to <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ieseventservice-fireesevent">IESEventService::FireESEvent</a>.
    

If an event originates from a PBDA device, the event object automatically calls the <a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_eventingservice-completeevent">IBDA_EventingService::CompleteEvent</a> method with the result set in the <b>SetCompletionStatus</b> call at the time it is released.  If the client is a managed application, it should dispose of the event object immediately after it is finished with the event. This disposition ensures that the <b>IBDA_EventingService::CompleteEvent</b> method is called in a timely manner


## -parameters




### -param dwResult [in]

Completion status for the event.
          


## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ieseventservice-fireesevent">FireESEvent</a>



<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesevent">IESEvent</a>
 

 