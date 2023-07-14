---
UID: NF:tuner.IESEventService.FireESEvent
title: IESEventService::FireESEvent (tuner.h)
description: Raises an event derived from the IESEvent interface.
helpviewer_keywords: ["FireESEvent","FireESEvent method [Microsoft TV Technologies]","FireESEvent method [Microsoft TV Technologies]","IESEventService interface","IESEventService interface [Microsoft TV Technologies]","FireESEvent method","IESEventService.FireESEvent","IESEventService::FireESEvent","mstv.ieseventservice_fireesevent","tuner/IESEventService::FireESEvent"]
old-location: mstv\ieseventservice_fireesevent.htm
tech.root: mstv
ms.assetid: 3781e50c-ab19-4bfa-86d6-af12223019ca
ms.date: 12/05/2018
ms.keywords: FireESEvent, FireESEvent method [Microsoft TV Technologies], FireESEvent method [Microsoft TV Technologies],IESEventService interface, IESEventService interface [Microsoft TV Technologies],FireESEvent method, IESEventService.FireESEvent, IESEventService::FireESEvent, mstv.ieseventservice_fireesevent, tuner/IESEventService::FireESEvent
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IESEventService::FireESEvent
 - tuner/IESEventService::FireESEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IESEventService.FireESEvent
---

# IESEventService::FireESEvent


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Raises an event derived from the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesevent">IESEvent</a> interface. Media Transform Devices in a  Protected Broadcast Driver Architecture (PBDA) graph can use this method to raise these types of events for Media Sink Devices that have registered to handle specific event types.

The <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesevent">IESEvent</a> object is processed in a multithreaded apartment and finally sent to clients from this apartment.  Make sure the object runs either using the multithreaded threading model or using the single-threaded with proper marshaling interfaces.

## -parameters

### -param pESEvent [in]

Pointer to the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesevent">IESEvent</a> interface for the event being raised.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesevent">IESEvent</a>