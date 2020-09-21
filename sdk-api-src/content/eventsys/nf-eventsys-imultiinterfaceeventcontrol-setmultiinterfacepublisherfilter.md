---
UID: NF:eventsys.IMultiInterfaceEventControl.SetMultiInterfacePublisherFilter
title: IMultiInterfaceEventControl::SetMultiInterfacePublisherFilter (eventsys.h)
description: Assigns a publisher filter to an event method at run time.
helpviewer_keywords: ["IMultiInterfaceEventControl interface [COM+]","SetMultiInterfacePublisherFilter method","IMultiInterfaceEventControl.SetMultiInterfacePublisherFilter","IMultiInterfaceEventControl::SetMultiInterfacePublisherFilter","SetMultiInterfacePublisherFilter","SetMultiInterfacePublisherFilter method [COM+]","SetMultiInterfacePublisherFilter method [COM+]","IMultiInterfaceEventControl interface","_cos_IMultiInterfaceEventControl_SetMultiInterfacePublisherFilter","cos.imultiinterfaceeventcontrol_setmultiinterfacepublisherfilter","eventsys/IMultiInterfaceEventControl::SetMultiInterfacePublisherFilter"]
old-location: cos\imultiinterfaceeventcontrol_setmultiinterfacepublisherfilter.htm
tech.root: cos
ms.assetid: 0eb52937-3bd8-45ab-b4ba-c0264c47c909
ms.date: 12/05/2018
ms.keywords: IMultiInterfaceEventControl interface [COM+],SetMultiInterfacePublisherFilter method, IMultiInterfaceEventControl.SetMultiInterfacePublisherFilter, IMultiInterfaceEventControl::SetMultiInterfacePublisherFilter, SetMultiInterfacePublisherFilter, SetMultiInterfacePublisherFilter method [COM+], SetMultiInterfacePublisherFilter method [COM+],IMultiInterfaceEventControl interface, _cos_IMultiInterfaceEventControl_SetMultiInterfacePublisherFilter, cos.imultiinterfaceeventcontrol_setmultiinterfacepublisherfilter, eventsys/IMultiInterfaceEventControl::SetMultiInterfacePublisherFilter
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
 - IMultiInterfaceEventControl::SetMultiInterfacePublisherFilter
 - eventsys/IMultiInterfaceEventControl::SetMultiInterfacePublisherFilter
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
 - IMultiInterfaceEventControl.SetMultiInterfacePublisherFilter
---

# IMultiInterfaceEventControl::SetMultiInterfacePublisherFilter


## -description

Assigns a publisher filter to an event method at run time.

This method sets the specified publisher filter for all methods of all event interfaces for the event object.

## -parameters

### -param classFilter [in]

A pointer to the <a href="/windows/desktop/api/eventsys/nn-eventsys-imultiinterfacepublisherfilter">IMultiInterfacePublisherFilter</a> interface on the publisher filter associated with the specified method.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and E_FAIL, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>EVENT_E_INTERNALEXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An unexpected exception was raised.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>EVENT_E_INTERNALERROR</b></dt>
</dl>
</td>
<td width="60%">
An unexpected internal error was detected.

</td>
</tr>
</table>

## -remarks

An event publisher can install a publisher filter at run time to fire an event only to subscribers that meet the criteria specified in the filter.

## -see-also

<a href="/windows/desktop/api/eventsys/nn-eventsys-imultiinterfaceeventcontrol">IMultiInterfaceEventControl</a>