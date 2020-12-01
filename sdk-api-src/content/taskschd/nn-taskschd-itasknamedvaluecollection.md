---
UID: NN:taskschd.ITaskNamedValueCollection
title: ITaskNamedValueCollection (taskschd.h)
description: Contains a collection of ITaskNamedValuePair interface name-value pairs.
helpviewer_keywords: ["ITaskNamedValueCollection","ITaskNamedValueCollection interface [Task Scheduler]","ITaskNamedValueCollection interface [Task Scheduler]","described","taskschd.itasknamedvaluecollection","taskschd/ITaskNamedValueCollection"]
old-location: taskschd\itasknamedvaluecollection.htm
tech.root: taskschd
ms.assetid: 440dc70b-02de-4974-ad2a-462491d12775
ms.date: 12/05/2018
ms.keywords: ITaskNamedValueCollection, ITaskNamedValueCollection interface [Task Scheduler], ITaskNamedValueCollection interface [Task Scheduler],described, taskschd.itasknamedvaluecollection, taskschd/ITaskNamedValueCollection
req.header: taskschd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITaskNamedValueCollection
 - taskschd/ITaskNamedValueCollection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - taskschd.dll
api_name:
 - ITaskNamedValueCollection
---

# ITaskNamedValueCollection interface


## -description

Contains a collection of <a href="/windows/desktop/api/taskschd/nn-taskschd-itasknamedvaluepair">ITaskNamedValuePair</a> interface name-value pairs.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITaskNamedValueCollection</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITaskNamedValueCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ITaskNamedValueCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/taskschd/nf-taskschd-itasknamedvaluecollection-clear">Clear</a>
</td>
<td align="left" width="63%">
Clears the entire collection of name-value pairs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/taskschd/nf-taskschd-itasknamedvaluecollection-create">Create</a>
</td>
<td align="left" width="63%">
Creates a name-value pair in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/taskschd/nf-taskschd-itasknamedvaluecollection-remove">Remove</a>
</td>
<td align="left" width="63%">
Removes a selected name-value pair from the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITaskNamedValueCollection</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/taskschd/nf-taskschd-itasknamedvaluecollection-get__newenum">_NewEnum</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the collection enumerator for the name-value pair collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/taskschd/nf-taskschd-itasknamedvaluecollection-get_count">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the number of name-value pairs in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/taskschd/nf-taskschd-itasknamedvaluecollection-get_item">Item</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the specified name-value pair from the collection.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields">HeaderFields Property of IEmailAction</a>



<a href="/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_valuequeries">ValueQueries Property of IEventTrigger</a>