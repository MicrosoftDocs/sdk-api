---
UID: NN:azroles.IAzTask
title: IAzTask (azroles.h)
description: Describes a set of operations.
helpviewer_keywords: ["IAzTask","IAzTask interface [Security]","IAzTask interface [Security]","described","azroles/IAzTask","security.iaztask"]
old-location: security\iaztask.htm
tech.root: security
ms.assetid: 90eb19c9-1490-43f4-ab4b-393e825aeb2f
ms.date: 12/05/2018
ms.keywords: IAzTask, IAzTask interface [Security], IAzTask interface [Security],described, azroles/IAzTask, security.iaztask
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
f1_keywords:
 - IAzTask
 - azroles/IAzTask
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzTask
---

# IAzTask interface


## -description

The <b>IAzTask</b> interface describes a set of operations.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzTask</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IAzTask</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IAzTask</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/azroles/nf-azroles-iaztask-addoperation">AddOperation</a>
</td>
<td align="left" width="63%">
Adds the <a href="/windows/desktop/api/azroles/nn-azroles-iazoperation">IAzOperation</a> object with the specified name to the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/azroles/nf-azroles-iaztask-addpropertyitem">AddPropertyItem</a>
</td>
<td align="left" width="63%">
Adds the specified entity to the specified list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/azroles/nf-azroles-iaztask-addtask">AddTask</a>
</td>
<td align="left" width="63%">
Adds the <b>IAzTask</b> object with the specified name to the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/azroles/nf-azroles-iaztask-deleteoperation">DeleteOperation</a>
</td>
<td align="left" width="63%">
Removes the <a href="/windows/desktop/api/azroles/nn-azroles-iazoperation">IAzOperation</a> object with the specified name from the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/azroles/nf-azroles-iaztask-deletepropertyitem">DeletePropertyItem</a>
</td>
<td align="left" width="63%">
Removes the specified entity from the specified list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/azroles/nf-azroles-iaztask-deletetask">DeleteTask</a>
</td>
<td align="left" width="63%">
Removes the <b>IAzTask</b> object with the specified name from the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/azroles/nf-azroles-iaztask-getproperty">GetProperty</a>
</td>
<td align="left" width="63%">
Returns the <b>IAzTask</b> object property with the specified property ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/azroles/nf-azroles-iaztask-setproperty">SetProperty</a>
</td>
<td align="left" width="63%">
Sets the specified value to the <b>IAzTask</b> object property with the specified property ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/azroles/nf-azroles-iaztask-submit">Submit</a>
</td>
<td align="left" width="63%">
Persists changes made to the <b>IAzTask</b> object.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzTask</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/azroles/nf-azroles-iaztask-get_applicationdata">ApplicationData</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves an opaque field that can be used by the application to store information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/azroles/nf-azroles-iaztask-get_bizrule">BizRule</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the text of the script that implements the business rule (BizRule).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/azroles/nf-azroles-iaztask-get_bizruleimportedpath">BizRuleImportedPath</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the path to the file from which the BizRule is imported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/azroles/nf-azroles-iaztask-get_bizrulelanguage">BizRuleLanguage</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the scripting language in which the BizRule is implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/azroles/nf-azroles-iaztask-get_description">Description</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a comment that describes the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/azroles/nf-azroles-iaztask-get_isroledefinition">IsRoleDefinition</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a value that indicates whether the task is a role definition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/azroles/nf-azroles-iaztask-get_name">Name</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the name of the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/azroles/nf-azroles-iaztask-get_operations">Operations</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the operations associated with the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/azroles/nf-azroles-iaztask-get_tasks">Tasks</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the tasks associated with the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/azroles/nf-azroles-iaztask-get_writable">Writable</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the task can be modified by the user context that initialized it.

</td>
</tr>
</table>