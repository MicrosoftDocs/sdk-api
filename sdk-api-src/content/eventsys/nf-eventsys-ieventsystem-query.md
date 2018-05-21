---
UID: NF:eventsys.IEventSystem.Query
title: IEventSystem::Query
author: windows-driver-content
description: Retrieves a collection of subscription or event objects from the event data store.
old-location: cos\ieventsystem_query.htm
old-project: cossdk
ms.assetid: 47025361-4420-4c5d-aed7-d40ea0ba3e3b
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IEventSystem interface [COM+],Query method, IEventSystem.Query, IEventSystem::Query, Query, Query method [COM+], Query method [COM+],IEventSystem interface, _cos_IEventSystem_Query, cos.ieventsystem_query, eventsys/IEventSystem::Query
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
-	IEventSystem.Query
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IEventSystem::Query


## -description


Retrieves a collection of subscription or event objects from the event data store.


## -parameters




### -param progID [in]

The ProgID of the object class to be queried. This must be a valid event object class identifier. This parameter can be one of the following values:

<ul>
<li>PROGID_EventClass</li>
<li>PROGID_EventClassCollection</li>
<li>PROGID_EventSubscription</li>
<li>PROGID_EventSubscriptionCollection</li>
</ul>

### -param queryCriteria [in]

The query criteria. For details on forming a valid expression for this parameter, see the Remarks section below.


### -param errorIndex [out]

The location, expressed as an offset, of an error in the <i>queryCriteria</i> parameter.


### -param ppInterface [out, retval]

Address of a pointer to the object obtained as a result of the query. This parameter cannot be <b>NULL</b>. Depending on the object specified by the <i>progID</i> parameter, this is a pointer to one of the following interfaces:

<ul>
<li>
<a href="https://msdn.microsoft.com/e8c1fcd1-59fb-49d6-94b9-52b7c8551651">IEventClass</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7bb00b80-a48f-49c8-983d-9ff0ea424e4d">IEventObjectCollection</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ce3f9f7e-3d0a-445f-b3db-671ee595aedf">IEventSubscription</a>
</li>
</ul>

## -returns



This method can return the standard return values E_INVALIDARG, E_POINTER, E_OUTOFMEMORY, E_UNEXPECTED, and E_FAIL, as well as the following values.

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
</table>
 




## -remarks



The caller is responsible for freeing memory allocated through the <i>ppInterface</i> parameter. 



The query criteria specified by the <i>queryCriteria</i> parameter can be "ALL", to specify a request for all subscription objects, or a Boolean expression denoting one or more conditions a subscription object must meet to be included in the query result. Valid expressions are of the following form:

[NOT] <i>propertyname</i><i>relationalOperator</i><i>value</i>. Valid relational operators are as follows: 

==, =, !=, &lt;&gt;, ~=. Valid values are "<i>string</i>", '<i>string</i>', {<i>GUID</i>}, <b>TRUE</b>, <b>FALSE</b>, <b>NULL</b>.

Individual Boolean expressions can be joined with AND or OR. Expressions can be nested in parentheses to enforce a specific order of evaluation.

Following are some examples of valid query criteria:

"EventClassID == {F89859D1-6565-11D1-88C8-0080C7D771BF}"

"EventClassID == {F89859D1-6565-11D1-88C8-0080C7D771BF} AND MethodName = 'StockPriceChange'"




## -see-also




<a href="https://msdn.microsoft.com/29b3e552-b717-4d10-9fa4-1386da3c5460">IEventSystem</a>
 

 

