---
UID: NF:eventsys.IMultiInterfaceEventControl.SetDefaultQuery
title: IMultiInterfaceEventControl::SetDefaultQuery (eventsys.h)
description: Establishes a default query to be used when a publisher filter is not associated with an event method.
helpviewer_keywords: ["IMultiInterfaceEventControl interface [COM+]","SetDefaultQuery method","IMultiInterfaceEventControl.SetDefaultQuery","IMultiInterfaceEventControl::SetDefaultQuery","SetDefaultQuery","SetDefaultQuery method [COM+]","SetDefaultQuery method [COM+]","IMultiInterfaceEventControl interface","_cos_IMultiInterfaceEventControl_SetDefaultQuery","cos.imultiinterfaceeventcontrol_setdefaultquery","eventsys/IMultiInterfaceEventControl::SetDefaultQuery"]
old-location: cos\imultiinterfaceeventcontrol_setdefaultquery.htm
tech.root: cos
ms.assetid: 31d544d4-8cac-46ae-9db7-c5b366ac6b2f
ms.date: 12/05/2018
ms.keywords: IMultiInterfaceEventControl interface [COM+],SetDefaultQuery method, IMultiInterfaceEventControl.SetDefaultQuery, IMultiInterfaceEventControl::SetDefaultQuery, SetDefaultQuery, SetDefaultQuery method [COM+], SetDefaultQuery method [COM+],IMultiInterfaceEventControl interface, _cos_IMultiInterfaceEventControl_SetDefaultQuery, cos.imultiinterfaceeventcontrol_setdefaultquery, eventsys/IMultiInterfaceEventControl::SetDefaultQuery
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
 - IMultiInterfaceEventControl::SetDefaultQuery
 - eventsys/IMultiInterfaceEventControl::SetDefaultQuery
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
 - IMultiInterfaceEventControl.SetDefaultQuery
---

# IMultiInterfaceEventControl::SetDefaultQuery


## -description

Establishes a default query to be used when a publisher filter is not associated with an event method.

## -parameters

### -param eventIID [in]

The interface identifier of the firing interface.

### -param bstrMethodName [in]

The name of the method to which the default query is assigned.

### -param bstrCriteria [in]

A string specifying the query criteria. This parameter cannot be <b>NULL</b>. For details on forming a valid expression for this parameter, see the Remarks section below.

### -param errorIndex [out, retval]

The location, expressed as an offset, of an error in the <i>bstrCriteria</i> parameter.

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

This method is a more specialized form of the <a href="/windows/desktop/api/eventsys/nf-eventsys-ieventsystem-query">IEventSystem::Query</a> method. In addition to obtaining only subscription objects, a collection obtained by calling <a href="/windows/desktop/api/eventsys/nf-eventsys-imultiinterfaceeventcontrol-getsubscriptions">GetSubscriptions</a> is automatically updated whenever the subscription collection changes.

The query criteria specified by the <i>bstrCriteria</i> parameter can be "ALL", to specify a request for all subscription objects, or a Boolean expression denoting one or more conditions a subscription object must meet to be included in the query result. Valid expressions are of the following form:

[NOT] <i>propertyname</i><i>relationalOperator</i><i>value</i>. Valid relational operators are as follows: 

==, =, !=, &lt;&gt;, ~=. Valid values are "<i>string</i>", '<i>string</i>', {<i>GUID</i>}, <b>TRUE</b>, <b>FALSE</b>, <b>NULL</b>.

Individual Boolean expressions can be joined with AND or OR. Expressions can be nested in parentheses to enforce a specific order of evaluation.

Following are some examples of valid query criteria:

"EventClassID == {F89859D1-6565-11D1-88C8-0080C7D771BF}"

"EventClassID == {F89859D1-6565-11D1-88C8-0080C7D771BF} AND MethodName = 'StockPriceChange'"

## -see-also

<a href="/windows/desktop/api/eventsys/nn-eventsys-imultiinterfaceeventcontrol">IMultiInterfaceEventControl</a>