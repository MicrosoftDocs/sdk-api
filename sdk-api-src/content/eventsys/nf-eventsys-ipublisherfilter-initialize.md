---
UID: NF:eventsys.IPublisherFilter.Initialize
title: IPublisherFilter::Initialize
author: windows-driver-content
description: Associates an event method with a collection of subscription objects.
old-location: cos\ipublisherfilter_initialize.htm
old-project: cossdk
ms.assetid: 803201c7-7fa8-4db5-858f-3d5af302ee88
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IPublisherFilter interface [COM+],Initialize method, IPublisherFilter.Initialize, IPublisherFilter::Initialize, Initialize, Initialize method [COM+], Initialize method [COM+],IPublisherFilter interface, _cos_IPublisherFilter_Initialize, cos.ipublisherfilter_initialize, eventsys/IPublisherFilter::Initialize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: EOC_ChangeType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	EventSys.h
api_name:
-	IPublisherFilter.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IPublisherFilter::Initialize


## -description


Associates an event method with a collection of subscription objects.

This method is supported only for backward compatibility. Otherwise, you should use the methods of the <a href="https://msdn.microsoft.com/f20f778b-fdd5-4c34-871b-d03cd1cd31cc">IMultiInterfacePublisherFilter</a> interface.


## -parameters




### -param methodName [in]

The name of the event method associated with the publisher filter. 


### -param dispUserDefined [in]

A pointer to the <a href="https://msdn.microsoft.com/29b3e552-b717-4d10-9fa4-1386da3c5460">IEventSystem</a> interface on an event system object or to the <a href="https://msdn.microsoft.com/8b2fba30-3ede-466f-ad3b-2de2175a088b">IEventControl</a> interface on an event class object. 


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



The publisher filter uses the pointer passed in dispUserDefined to obtain a list of subscribers, either by calling <a href="https://msdn.microsoft.com/47025361-4420-4c5d-aed7-d40ea0ba3e3b">IEventSystem::Query</a> or <a href="https://msdn.microsoft.com/ba39305d-8dc3-40fe-b6f6-d5c22f54a180">IEventControl::GetSubscriptions</a>. 





## -see-also




<a href="https://msdn.microsoft.com/f20f778b-fdd5-4c34-871b-d03cd1cd31cc">IMultiInterfacePublisherFilter</a>



<a href="https://msdn.microsoft.com/affc0af4-36f8-4479-8685-f91c29111d76">IPublisherFilter</a>
 

 

