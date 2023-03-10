---
UID: NN:comsvcs.ISendMethodEvents
title: ISendMethodEvents (comsvcs.h)
description: Describes an event class that notifies subscribers whenever a method on the object that implements it either is called or returns from a call.
helpviewer_keywords: ["ISendMethodEvents","ISendMethodEvents interface [COM+]","ISendMethodEvents interface [COM+]","described","_cos_ISendMethodEvents","comsvcs/ISendMethodEvents","cos.isendmethodevents"]
old-location: cos\isendmethodevents.htm
tech.root: cos
ms.assetid: d1437581-8a2b-4e88-aa12-a16eb9f40125
ms.date: 12/05/2018
ms.keywords: ISendMethodEvents, ISendMethodEvents interface [COM+], ISendMethodEvents interface [COM+],described, _cos_ISendMethodEvents, comsvcs/ISendMethodEvents, cos.isendmethodevents
req.header: comsvcs.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISendMethodEvents
 - comsvcs/ISendMethodEvents
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ISendMethodEvents
---

# ISendMethodEvents interface


## -description

Describes an event class that notifies subscribers whenever a method on the object that implements it either is called or returns from a call. The events are published to the subscriber using the <a href="/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.

## -inheritance

The <b>ISendMethodEvents</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISendMethodEvents</b> also has these types of members:

## -remarks

To send method events to the COM+ tracker property, you need to obtain a handle to it and you need to obtain its GUID, which is defined as follows.


``` syntax
GUID guidTrkPropPolicy = {0xecabaeb3, 0x7f19, 0x11d2, {0x97, 0x8e, 0x00, 0x00, 0xf8, 0x75, 0x7e, 0x2a}}

```

To obtain a handle to the COM+ tracker property, call the <a href="/windows/desktop/api/objidl/nf-objidl-icontext-getproperty">IContext::GetProperty</a> method with the <i>rGuid</i> argument set equal to this GUID.

## -see-also

<a href="/windows/desktop/cossdk/com--events">COM+ Events</a>
