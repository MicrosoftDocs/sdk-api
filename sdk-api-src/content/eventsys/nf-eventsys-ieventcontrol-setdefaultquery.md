---
UID: NF:eventsys.IEventControl.SetDefaultQuery
title: IEventControl::SetDefaultQuery (eventsys.h)
description: Sets the default query to determine subscribers.
helpviewer_keywords: ["IEventControl interface [COM+]","SetDefaultQuery method","IEventControl.SetDefaultQuery","IEventControl::SetDefaultQuery","SetDefaultQuery","SetDefaultQuery method [COM+]","SetDefaultQuery method [COM+]","IEventControl interface","_cos_IEventControl_SetDefaultQuery","cos.ieventcontrol_setdefaultquery","eventsys/IEventControl::SetDefaultQuery"]
old-location: cos\ieventcontrol_setdefaultquery.htm
tech.root: cos
ms.assetid: ea0cc4b8-e345-44bc-969e-f35f25b641f9
ms.date: 12/05/2018
ms.keywords: IEventControl interface [COM+],SetDefaultQuery method, IEventControl.SetDefaultQuery, IEventControl::SetDefaultQuery, SetDefaultQuery, SetDefaultQuery method [COM+], SetDefaultQuery method [COM+],IEventControl interface, _cos_IEventControl_SetDefaultQuery, cos.ieventcontrol_setdefaultquery, eventsys/IEventControl::SetDefaultQuery
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
 - IEventControl::SetDefaultQuery
 - eventsys/IEventControl::SetDefaultQuery
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
 - IEventControl.SetDefaultQuery
---

# IEventControl::SetDefaultQuery


## -description

Sets the default query to determine subscribers.

## -parameters

### -param methodName [in]

The name of the method to which the default query is assigned.

### -param criteria [in]

The query criteria. This parameter cannot be <b>NULL</b>. For details on forming a valid expression for this parameter, see the Remarks section below.

### -param errorIndex [out, retval]

The location, expressed as an offset, of an error in the <i>criteria</i> parameter.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The query criteria specified by the <i>criteria</i> parameter can be "ALL", to specify a request for all subscription objects, or a Boolean expression denoting one or more conditions a subscription object must meet to be included in the query result. Valid expressions are of the following form:

[NOT] <i>propertyname</i><i>relationalOperator</i><i>value</i>. Valid relational operators are as follows: 

==, =, !=, &lt;&gt;, ~=. Valid values are "<i>string</i>", '<i>string</i>', {<i>GUID</i>}, <b>TRUE</b>, <b>FALSE</b>, <b>NULL</b>.

Individual Boolean expressions can be joined with AND or OR. Expressions can be nested in parentheses to enforce a specific order of evaluation.

Following are some examples of valid query criteria:

"EventClassID == {F89859D1-6565-11D1-88C8-0080C7D771BF}"

"EventClassID == {F89859D1-6565-11D1-88C8-0080C7D771BF} AND MethodName = 'StockPriceChange'"

## -see-also

<a href="/windows/desktop/api/eventsys/nn-eventsys-ieventcontrol">IEventControl</a>