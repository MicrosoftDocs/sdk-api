---
UID: NF:eventsys.IPublisherFilter.Initialize
title: IPublisherFilter::Initialize (eventsys.h)
description: Associates an event method with a collection of subscription objects.
helpviewer_keywords: ["IPublisherFilter interface [COM+]","Initialize method","IPublisherFilter.Initialize","IPublisherFilter::Initialize","Initialize","Initialize method [COM+]","Initialize method [COM+]","IPublisherFilter interface","_cos_IPublisherFilter_Initialize","cos.ipublisherfilter_initialize","eventsys/IPublisherFilter::Initialize"]
old-location: cos\ipublisherfilter_initialize.htm
tech.root: cos
ms.assetid: 803201c7-7fa8-4db5-858f-3d5af302ee88
ms.date: 12/05/2018
ms.keywords: IPublisherFilter interface [COM+],Initialize method, IPublisherFilter.Initialize, IPublisherFilter::Initialize, Initialize, Initialize method [COM+], Initialize method [COM+],IPublisherFilter interface, _cos_IPublisherFilter_Initialize, cos.ipublisherfilter_initialize, eventsys/IPublisherFilter::Initialize
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
 - IPublisherFilter::Initialize
 - eventsys/IPublisherFilter::Initialize
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
 - IPublisherFilter.Initialize
---

# IPublisherFilter::Initialize


## -description

Associates an event method with a collection of subscription objects.

This method is supported only for backward compatibility. Otherwise, you should use the methods of the <a href="/windows/desktop/api/eventsys/nn-eventsys-imultiinterfacepublisherfilter">IMultiInterfacePublisherFilter</a> interface.

## -parameters

### -param methodName [in]

The name of the event method associated with the publisher filter.

### -param dispUserDefined [in]

A pointer to the <a href="/windows/desktop/api/eventsys/nn-eventsys-ieventsystem">IEventSystem</a> interface on an event system object or to the <a href="/windows/desktop/api/eventsys/nn-eventsys-ieventcontrol">IEventControl</a> interface on an event class object.

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
The publisher filter was successfully initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>EVENT_S_SOME_SUBSCRIBERS_FAILED</b></dt>
</dl>
</td>
<td width="60%">
An event was able to invoke some, but not all, of the subscribers.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>EVENT_E_ALL_SUBSCRIBERS_FAILED</b></dt>
</dl>
</td>
<td width="60%">
An event was unable to invoke any of the subscribers.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>EVENT_S_NOSUBSCRIBERS</b></dt>
</dl>
</td>
<td width="60%">
An event was published but there were no subscribers.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>EVENT_E_QUERYSYNTAX</b></dt>
</dl>
</td>
<td width="60%">
A syntax error occurred while trying to evaluate a query string.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>EVENT_E_QUERYFIELD</b></dt>
</dl>
</td>
<td width="60%">
An invalid field name was used in a query string.

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
<tr>
<td width="40%">
<dl>
<dt><b>EVENT_E_INVALID_PER_USER_SID</b></dt>
</dl>
</td>
<td width="60%">
The owner SID on a per-user subscription does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>EVENT_E_USER_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
A user-supplied component or subscriber raised an exception.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>EVENT_E_TOO_MANY_METHODS</b></dt>
</dl>
</td>
<td width="60%">
An interface has too many methods from which to fire events.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>EVENT_E_MISSING_EVENTCLASS</b></dt>
</dl>
</td>
<td width="60%">
A subscription cannot be stored unless the event class for the subscription already exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>EVENT_E_NOT_ALL_REMOVED</b></dt>
</dl>
</td>
<td width="60%">
Not all of the requested objects could be removed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>EVENT_E_COMPLUS_NOT_INSTALLED</b></dt>
</dl>
</td>
<td width="60%">
COM+ is required for this operation, but it is not installed.

</td>
</tr>
</table>

## -remarks

The publisher filter uses the pointer passed in dispUserDefined to obtain a list of subscribers, either by calling <a href="/windows/desktop/api/eventsys/nf-eventsys-ieventsystem-query">IEventSystem::Query</a> or <a href="/windows/desktop/api/eventsys/nf-eventsys-ieventcontrol-getsubscriptions">IEventControl::GetSubscriptions</a>.

## -see-also

<a href="/windows/desktop/api/eventsys/nn-eventsys-imultiinterfacepublisherfilter">IMultiInterfacePublisherFilter</a>



<a href="/windows/desktop/api/eventsys/nn-eventsys-ipublisherfilter">IPublisherFilter</a>