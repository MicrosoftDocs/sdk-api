---
UID: NF:eventsys.IPublisherFilter.PrepareToFire
title: IPublisherFilter::PrepareToFire (eventsys.h)
description: Prepares a publisher filter to begin firing a filtered list of subscriptions using a provided firing control. The firing control is contained in the event class object.
helpviewer_keywords: ["IPublisherFilter interface [COM+]","PrepareToFire method","IPublisherFilter.PrepareToFire","IPublisherFilter::PrepareToFire","PrepareToFire","PrepareToFire method [COM+]","PrepareToFire method [COM+]","IPublisherFilter interface","_cos_IPublisherFilter_PrepareToFire","cos.ipublisherfilter_preparetofire","eventsys/IPublisherFilter::PrepareToFire"]
old-location: cos\ipublisherfilter_preparetofire.htm
tech.root: cos
ms.assetid: 78faa83f-ee73-4034-9be1-5576e5a909e3
ms.date: 12/05/2018
ms.keywords: IPublisherFilter interface [COM+],PrepareToFire method, IPublisherFilter.PrepareToFire, IPublisherFilter::PrepareToFire, PrepareToFire, PrepareToFire method [COM+], PrepareToFire method [COM+],IPublisherFilter interface, _cos_IPublisherFilter_PrepareToFire, cos.ipublisherfilter_preparetofire, eventsys/IPublisherFilter::PrepareToFire
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
 - IPublisherFilter::PrepareToFire
 - eventsys/IPublisherFilter::PrepareToFire
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
 - IPublisherFilter.PrepareToFire
---

# IPublisherFilter::PrepareToFire


## -description

Prepares a publisher filter to begin firing a filtered list of subscriptions using a provided firing control. The firing control is contained in the event class object.

This method is supported only for backward compatibility. Otherwise, you should use the methods of the <a href="/windows/desktop/api/eventsys/nn-eventsys-imultiinterfacepublisherfilter">IMultiInterfacePublisherFilter</a> interface.

## -parameters

### -param methodName [in]

The name of the event method to be fired.

### -param firingControl [in]

A pointer to the <a href="/windows/desktop/api/eventsys/nn-eventsys-ifiringcontrol">IFiringControl</a> interface on the firing control object.

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
The event class object is ready to fire the event.

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

## -see-also

<a href="/windows/desktop/api/eventsys/nn-eventsys-imultiinterfacepublisherfilter">IMultiInterfacePublisherFilter</a>



<a href="/windows/desktop/api/eventsys/nn-eventsys-ipublisherfilter">IPublisherFilter</a>