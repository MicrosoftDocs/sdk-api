---
UID: NF:tuner.IESEvent.GetEventType
title: IESEvent::GetEventType (tuner.h)
description: Gets the GUID that identifies an event that is derived from the IESEvent interface. The GUID is contained in an IESEvent object, which ispassed in a call to IESEventService::FireESEvent.
helpviewer_keywords: ["GetEventType","GetEventType method [Microsoft TV Technologies]","GetEventType method [Microsoft TV Technologies]","IESEvent interface","IESEvent interface [Microsoft TV Technologies]","GetEventType method","IESEvent.GetEventType","IESEvent::GetEventType","mstv.iesevent_geteventtype","tuner/IESEvent::GetEventType"]
old-location: mstv\iesevent_geteventtype.htm
tech.root: mstv
ms.assetid: 8418116a-2393-4a1b-8c5b-2356d373e426
ms.date: 12/05/2018
ms.keywords: GetEventType, GetEventType method [Microsoft TV Technologies], GetEventType method [Microsoft TV Technologies],IESEvent interface, IESEvent interface [Microsoft TV Technologies],GetEventType method, IESEvent.GetEventType, IESEvent::GetEventType, mstv.iesevent_geteventtype, tuner/IESEvent::GetEventType
f1_keywords:
- tuner/IESEvent.GetEventType
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
- IESEvent.GetEventType
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IESEvent::GetEventType


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]


Gets the GUID that identifies an event that is derived from the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesevent">IESEvent</a> interface. The GUID is contained in an <b>IESEvent</b> object, which ispassed in a call to <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ieseventservice-fireesevent">IESEventService::FireESEvent</a>.


## -parameters




### -param pguidEventType [out, retval]

Pointer to the GUID that uniquely identifies the event type.


## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesevent">IESEvent</a>



<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ieseventservice-fireesevent">IESEventService::FireESEvent</a>
 

 