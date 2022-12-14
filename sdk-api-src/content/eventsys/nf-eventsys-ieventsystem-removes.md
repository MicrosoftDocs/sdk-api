---
UID: NF:eventsys.IEventSystem.RemoveS
title: IEventSystem::RemoveS (eventsys.h)
description: Removes one or more subscription or event objects from the event data store. (IEventSystem.RemoveS)
helpviewer_keywords: ["IEventSystem interface [COM+]","RemoveS method","IEventSystem.RemoveS","IEventSystem::RemoveS","RemoveS","RemoveS method [COM+]","RemoveS method [COM+]","IEventSystem interface","_cos_IEventSystem_RemoveS","cos.ieventsystem_removes","eventsys/IEventSystem::RemoveS"]
old-location: cos\ieventsystem_removes.htm
tech.root: cos
ms.assetid: 6c3d2972-bfc4-43f2-a131-f3b3010a3c91
ms.date: 12/05/2018
ms.keywords: IEventSystem interface [COM+],RemoveS method, IEventSystem.RemoveS, IEventSystem::RemoveS, RemoveS, RemoveS method [COM+], RemoveS method [COM+],IEventSystem interface, _cos_IEventSystem_RemoveS, cos.ieventsystem_removes, eventsys/IEventSystem::RemoveS
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
 - IEventSystem::RemoveS
 - eventsys/IEventSystem::RemoveS
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
 - IEventSystem.RemoveS
---

# IEventSystem::RemoveS


## -description

Removes one or more subscription or event objects from the event data store.

## -parameters

### -param progID [in]

The ProgID of the object class to be removed. This must be a valid event object class identifier. This parameter can be one of the following values:

<ul>
<li>PROGID_EventClass</li>
<li>PROGID_EventClassCollection</li>
<li>PROGID_EventSubscription</li>
<li>PROGID_EventSubscriptionCollection</li>
</ul>

### -param queryCriteria [in]

The query criteria. For details on forming a valid expression for this parameter, see the Remarks section below.

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
<dt><b>EVENT_E_NOT_ALL_REMOVED</b></dt>
</dl>
</td>
<td width="60%">
Not all of the requested objects could be removed.

</td>
</tr>
</table>

## -remarks

The query criteria specified by the <i>queryCriteria</i> parameter can be "ALL", to specify a request for all subscription objects, or a Boolean expression denoting one or more conditions a subscription object must meet to be included in the query result. Valid expressions are of the following form:

[NOT] <i>propertyname</i><i>relationalOperator</i><i>value</i>. Valid relational operators are as follows: 

==, =, !=, &lt;&gt;, ~=. Valid values are "<i>string</i>", '<i>string</i>', {<i>GUID</i>}, <b>TRUE</b>, <b>FALSE</b>, <b>NULL</b>.

Individual Boolean expressions can be joined with AND or OR. Expressions can be nested in parentheses to enforce a specific order of evaluation.

Following are some examples of valid query criteria:

"EventClassID == {F89859D1-6565-11D1-88C8-0080C7D771BF}"

"EventClassID == {F89859D1-6565-11D1-88C8-0080C7D771BF} AND MethodName = 'StockPriceChange'"

## -see-also

<a href="/windows/desktop/api/eventsys/nn-eventsys-ieventsystem">IEventSystem</a>
