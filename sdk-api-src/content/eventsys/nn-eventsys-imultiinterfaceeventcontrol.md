---
UID: NN:eventsys.IMultiInterfaceEventControl
title: IMultiInterfaceEventControl (eventsys.h)
description: Controls the behavior of an event object, the object that fires an event to its subscribers. (IMultiInterfaceEventControl)
helpviewer_keywords: ["IMultiInterfaceEventControl","IMultiInterfaceEventControl interface [COM+]","IMultiInterfaceEventControl interface [COM+]","described","_cos_IMultiInterfaceEventControl","cos.imultiinterfaceeventcontrol","eventsys/IMultiInterfaceEventControl"]
old-location: cos\imultiinterfaceeventcontrol.htm
tech.root: cos
ms.assetid: e603f68a-881c-468d-a3d3-738f43400e01
ms.date: 12/05/2018
ms.keywords: IMultiInterfaceEventControl, IMultiInterfaceEventControl interface [COM+], IMultiInterfaceEventControl interface [COM+],described, _cos_IMultiInterfaceEventControl, cos.imultiinterfaceeventcontrol, eventsys/IMultiInterfaceEventControl
req.header: eventsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: EventSys.idl
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
 - IMultiInterfaceEventControl
 - eventsys/IMultiInterfaceEventControl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - EventSys.h
api_name:
 - IMultiInterfaceEventControl
---

# IMultiInterfaceEventControl interface


## -description

Controls the behavior of an event object, the object that fires an event to its subscribers. The <b>IMultiInterfaceEventControl</b> interface differs from the <a href="/windows/desktop/api/eventsys/nn-eventsys-ieventcontrol">IEventControl</a> interface in that it supports multiple event interfaces for the event object.

## -inheritance

The <b>IMultiInterfaceEventControl</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMultiInterfaceEventControl</b> also has these types of members:

