---
UID: NF:eventsys.IEventControl.SetPublisherFilter
title: IEventControl::SetPublisherFilter (eventsys.h)
description: Assigns a publisher filter to an event method.
helpviewer_keywords: ["IEventControl interface [COM+]","SetPublisherFilter method","IEventControl.SetPublisherFilter","IEventControl::SetPublisherFilter","SetPublisherFilter","SetPublisherFilter method [COM+]","SetPublisherFilter method [COM+]","IEventControl interface","_cos_IEventControl_SetPublisherFilter","cos.ieventcontrol_setpublisherfilter","eventsys/IEventControl::SetPublisherFilter"]
old-location: cos\ieventcontrol_setpublisherfilter.htm
tech.root: cos
ms.assetid: 9ebe0f55-9e2f-4538-9c16-1b237abfd07b
ms.date: 12/05/2018
ms.keywords: IEventControl interface [COM+],SetPublisherFilter method, IEventControl.SetPublisherFilter, IEventControl::SetPublisherFilter, SetPublisherFilter, SetPublisherFilter method [COM+], SetPublisherFilter method [COM+],IEventControl interface, _cos_IEventControl_SetPublisherFilter, cos.ieventcontrol_setpublisherfilter, eventsys/IEventControl::SetPublisherFilter
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
 - IEventControl::SetPublisherFilter
 - eventsys/IEventControl::SetPublisherFilter
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
 - IEventControl.SetPublisherFilter
---

# IEventControl::SetPublisherFilter


## -description

Assigns a publisher filter to an event method.

## -parameters

### -param methodName [in]

The name of the event method associated with the publisher filter to be assigned.

### -param pPublisherFilter [in]

A pointer to the <a href="/windows/desktop/api/eventsys/nn-eventsys-ipublisherfilter">IPublisherFilter</a> interface on the publisher filter associated with the specified method.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

An event publisher can install a publisher filter at run time to fire an event only to subscribers that meet the criteria specified in the filter.

## -see-also

<a href="/windows/desktop/api/eventsys/nn-eventsys-ieventcontrol">IEventControl</a>