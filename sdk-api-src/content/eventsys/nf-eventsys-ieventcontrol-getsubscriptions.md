---
UID: NF:eventsys.IEventControl.GetSubscriptions
title: IEventControl::GetSubscriptions (eventsys.h)
description: Retrieves the collection of subscriptions associated with an event method.
old-location: cos\ieventcontrol_getsubscriptions.htm
tech.root: cossdk
ms.assetid: ba39305d-8dc3-40fe-b6f6-d5c22f54a180
ms.date: 12/05/2018
ms.keywords: GetSubscriptions, GetSubscriptions method [COM+], GetSubscriptions method [COM+],IEventControl interface, IEventControl interface [COM+],GetSubscriptions method, IEventControl.GetSubscriptions, IEventControl::GetSubscriptions, _cos_IEventControl_GetSubscriptions, cos.ieventcontrol_getsubscriptions, eventsys/IEventControl::GetSubscriptions
f1_keywords:
- eventsys/IEventControl.GetSubscriptions
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Eventsys.h
api_name:
- IEventControl.GetSubscriptions
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEventControl::GetSubscriptions


## -description


Retrieves the collection of subscriptions associated with an event method.


## -parameters




### -param methodName [in]

The event method associated with the subscription collection.


### -param optionalCriteria [in]

The query criteria. If this parameter is <b>NULL</b>, the default query specified by the <a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventcontrol-setdefaultquery">SetDefaultQuery</a> method is used. For details on forming a valid expression for this parameter, see the Remarks section below.


### -param optionalErrorIndex [in]

The location, expressed as an offset, of an error in the <i>OptionalCriteria</i> parameter. This parameter cannot be <b>NULL</b>.


### -param ppCollection [out, retval]

Address of a pointer to <a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nn-eventsys-ieventobjectcollection">IEventObjectCollection</a> interface on a collection object that enumerates the subscriptions associated with the event object.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is a more specialized form of the <a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventsystem-query">IEventSystem::Query</a> method. In addition to obtaining only subscription objects, a collection obtained by calling <b>GetSubscriptions</b> is automatically updated whenever the subscription collection changes.

The query criteria specified by the <i>optionalCriteria</i> parameter can be "ALL", to specify a request for all subscription objects, or a Boolean expression denoting one or more conditions a subscription object must meet to be included in the query result. Valid expressions are of the following form:

[NOT] <i>propertyname</i><i>relationalOperator</i><i>value</i>. Valid relational operators are as follows: 

==, =, !=, &lt;&gt;, ~=. Valid values are "<i>string</i>", '<i>string</i>', {<i>GUID</i>}, <b>TRUE</b>, <b>FALSE</b>, <b>NULL</b>.

Individual Boolean expressions can be joined with AND or OR. Expressions can be nested in parentheses to enforce a specific order of evaluation.

Following are some examples of valid query criteria:

"EventClassID == {F89859D1-6565-11D1-88C8-0080C7D771BF}"

"EventClassID == {F89859D1-6565-11D1-88C8-0080C7D771BF} AND MethodName = 'StockPriceChange'"




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nn-eventsys-ieventcontrol">IEventControl</a>
 

 

