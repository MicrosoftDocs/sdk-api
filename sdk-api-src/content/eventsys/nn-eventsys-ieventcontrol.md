---
UID: NN:eventsys.IEventControl
title: IEventControl (eventsys.h)
description: Controls the behavior of an event object, the object that fires an event to its subscribers. (IEventControl)
helpviewer_keywords: ["IEventControl","IEventControl interface [COM+]","IEventControl interface [COM+]","described","_cos_IEventControl","cos.ieventcontrol","eventsys/IEventControl"]
old-location: cos\ieventcontrol.htm
tech.root: cos
ms.assetid: 8b2fba30-3ede-466f-ad3b-2de2175a088b
ms.date: 12/05/2018
ms.keywords: IEventControl, IEventControl interface [COM+], IEventControl interface [COM+],described, _cos_IEventControl, cos.ieventcontrol, eventsys/IEventControl
req.header: eventsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Eventsys.idl
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
 - IEventControl
 - eventsys/IEventControl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Eventsys.h
api_name:
 - IEventControl
---

# IEventControl interface


## -description

Controls the behavior of an event object, the object that fires an event to its subscribers.

The <b>IEventControl</b> interface differs from the <a href="/windows/desktop/api/eventsys/nn-eventsys-imultiinterfaceeventcontrol">IMultiInterfaceEventControl</a> interface in that it supports only one interface for the event object.

## -inheritance

The <b>IEventControl</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IEventControl</b> also has these types of members:

