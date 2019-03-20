---
UID: NF:tuner.IESEvent.GetEventType
title: IESEvent::GetEventType (tuner.h)
author: windows-sdk-content
description: Gets the GUID that identifies an event that is derived from the IESEvent interface. The GUID is contained in an IESEvent object, which ispassed in a call to IESEventService::FireESEvent.
old-location: mstv\iesevent_geteventtype.htm
tech.root: mstv
ms.assetid: 8418116a-2393-4a1b-8c5b-2356d373e426
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetEventType, GetEventType method [Microsoft TV Technologies], GetEventType method [Microsoft TV Technologies],IESEvent interface, IESEvent interface [Microsoft TV Technologies],GetEventType method, IESEvent.GetEventType, IESEvent::GetEventType, mstv.iesevent_geteventtype, tuner/IESEvent::GetEventType
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IESEvent::GetEventType


## -description


Gets the GUID that identifies an event that is derived from the <a href="https://msdn.microsoft.com/3c375480-c6df-4bb0-b417-5765b0bed9bf">IESEvent</a> interface. The GUID is contained in an <b>IESEvent</b> object, which ispassed in a call to <a href="https://msdn.microsoft.com/3781e50c-ab19-4bfa-86d6-af12223019ca">IESEventService::FireESEvent</a>.


## -parameters




### -param pguidEventType [out, retval]

Pointer to the GUID that uniquely identifies the event type.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3c375480-c6df-4bb0-b417-5765b0bed9bf">IESEvent</a>



<a href="https://msdn.microsoft.com/3781e50c-ab19-4bfa-86d6-af12223019ca">IESEventService::FireESEvent</a>
 

 

