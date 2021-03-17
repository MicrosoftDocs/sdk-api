---
UID: NF:eventsys.IMultiInterfaceEventControl.GetSubscriptions
title: IMultiInterfaceEventControl::GetSubscriptions (eventsys.h)
description: Retrieves the collection of subscription objects associated with an event method.
helpviewer_keywords: ["GetSubscriptions","GetSubscriptions method [COM+]","GetSubscriptions method [COM+]","IMultiInterfaceEventControl interface","IMultiInterfaceEventControl interface [COM+]","GetSubscriptions method","IMultiInterfaceEventControl.GetSubscriptions","IMultiInterfaceEventControl::GetSubscriptions","_cos_IMultiInterfaceEventControl_GetSubscriptions","cos.imultiinterfaceeventcontrol_getsubscriptions","eventsys/IMultiInterfaceEventControl::GetSubscriptions"]
old-location: cos\imultiinterfaceeventcontrol_getsubscriptions.htm
tech.root: cos
ms.assetid: 38b1d0fe-c32e-41d5-a0c1-2b4e72908fce
ms.date: 12/05/2018
ms.keywords: GetSubscriptions, GetSubscriptions method [COM+], GetSubscriptions method [COM+],IMultiInterfaceEventControl interface, IMultiInterfaceEventControl interface [COM+],GetSubscriptions method, IMultiInterfaceEventControl.GetSubscriptions, IMultiInterfaceEventControl::GetSubscriptions, _cos_IMultiInterfaceEventControl_GetSubscriptions, cos.imultiinterfaceeventcontrol_getsubscriptions, eventsys/IMultiInterfaceEventControl::GetSubscriptions
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
 - IMultiInterfaceEventControl::GetSubscriptions
 - eventsys/IMultiInterfaceEventControl::GetSubscriptions
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
 - IMultiInterfaceEventControl.GetSubscriptions
---

# IMultiInterfaceEventControl::GetSubscriptions


## -description

Retrieves the collection of subscription objects associated with an event method.

## -parameters

### -param eventIID [in]

The interface identifier of the firing interface.

### -param bstrMethodName [in]

The event method associated with the subscription collection.

### -param optionalCriteria [in]

A string specifying the query criteria. If this parameter is <b>NULL</b>, the default query specified by the <a href="/windows/desktop/api/eventsys/nf-eventsys-imultiinterfaceeventcontrol-setdefaultquery">SetDefaultQuery</a> method is used. For details on forming a valid expression for this parameter, see the Remarks section below.

### -param optionalErrorIndex [in]

The location, expressed as an offset, of an error in the <i>optionalCriteria</i> parameter. This parameter cannot be <b>NULL</b>.

### -param ppCollection [out, retval]

The address of a pointer to an <a href="/windows/desktop/api/eventsys/nn-eventsys-ieventobjectcollection">IEventObjectCollection</a> interface on a collection object that enumerates the subscriptions associated with the event object.

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

This method is a more specialized form of the <a href="/windows/desktop/api/eventsys/nf-eventsys-ieventsystem-query">IEventSystem::Query</a> method. In addition to obtaining only subscription objects, a collection obtained by calling <b>GetSubscriptions</b> is automatically updated whenever the subscription collection changes.

The query criteria specified by the <i>optionalCriteria</i> parameter can be "ALL", to specify a request for all subscription objects, or a Boolean expression denoting one or more conditions a subscription object must meet to be included in the query result. Valid expressions are of the following form:

[NOT] <i>propertyname</i><i>relationalOperator</i><i>value</i>. Valid relational operators are as follows: 

==, =, !=, &lt;&gt;, ~=. Valid values are "<i>string</i>", '<i>string</i>', {<i>GUID</i>}, <b>TRUE</b>, <b>FALSE</b>, <b>NULL</b>.

Individual Boolean expressions can be joined with AND or OR. Expressions can be nested in parentheses to enforce a specific order of evaluation.

Following are some examples of valid query criteria:

"EventClassID == {F89859D1-6565-11D1-88C8-0080C7D771BF}"

"EventClassID == {F89859D1-6565-11D1-88C8-0080C7D771BF} AND MethodName = 'StockPriceChange'"

## -see-also

<a href="/windows/desktop/api/eventsys/nn-eventsys-imultiinterfaceeventcontrol">IMultiInterfaceEventControl</a>