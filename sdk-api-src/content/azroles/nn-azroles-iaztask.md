---
UID: NN:azroles.IAzTask
title: IAzTask
author: windows-sdk-content
description: Describes a set of operations.
old-location: security\iaztask.htm
old-project: SecAuthZ
ms.assetid: 90eb19c9-1490-43f4-ab4b-393e825aeb2f
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IAzTask, IAzTask interface [Security], IAzTask interface [Security],described, azroles/IAzTask, security.iaztask
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: AZ_PROP_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Azroles.dll
api_name:
-	IAzTask
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzTask interface


## -description


The <b>IAzTask</b> interface describes a set of operations.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzTask</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IAzTask</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/73da7094-440c-4e68-8d43-9f4ba26dd14b">AddOperation</a>
</td>
<td align="left" width="63%">
Adds the <a href="https://msdn.microsoft.com/054fa4aa-70be-4618-a635-3941c830ea4e">IAzOperation</a> object with the specified name to the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50d8c1f2-11c3-41d8-b935-a8f296d2c18f">AddPropertyItem</a>
</td>
<td align="left" width="63%">
Adds the specified entity to the specified list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b3057d1-26aa-443c-857f-0057ef9d2072">AddTask</a>
</td>
<td align="left" width="63%">
Adds the <b>IAzTask</b> object with the specified name to the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f370d04-2115-4dcc-bf18-2d28a52bdead">DeleteOperation</a>
</td>
<td align="left" width="63%">
Removes the <a href="https://msdn.microsoft.com/054fa4aa-70be-4618-a635-3941c830ea4e">IAzOperation</a> object with the specified name from the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a9ffd54-cd1c-46ab-ab22-5c999b60d802">DeletePropertyItem</a>
</td>
<td align="left" width="63%">
Removes the specified entity from the specified list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1e1288ff-d67b-4180-bfd0-63b81df8f99b">DeleteTask</a>
</td>
<td align="left" width="63%">
Removes the <b>IAzTask</b> object with the specified name from the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d484f56c-3d96-48df-a0d1-1bea58e30f26">GetProperty</a>
</td>
<td align="left" width="63%">
Returns the <b>IAzTask</b> object property with the specified property ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/515d23f6-fcd9-4838-8910-2675211dfc48">SetProperty</a>
</td>
<td align="left" width="63%">
Sets the specified value to the <b>IAzTask</b> object property with the specified property ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a6f01573-c1ee-421d-8591-e1c9fa6c3d68">Submit</a>
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

<a href="https://msdn.microsoft.com/0a3939ee-6449-4eef-bb23-11e6d7018f04">ApplicationData</a>


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

<a href="https://msdn.microsoft.com/cf3d87af-5320-4fe0-b513-e242f8a1dd1b">BizRule</a>


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

<a href="https://msdn.microsoft.com/52422e14-4a96-455d-ad35-b8816871ee10">BizRuleImportedPath</a>


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

<a href="https://msdn.microsoft.com/922f4fd8-f553-439c-b9ae-51a45a88adc7">BizRuleLanguage</a>


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

<a href="https://msdn.microsoft.com/library/windows/hardware/dn915161">Description</a>


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

<a href="https://msdn.microsoft.com/fef32545-de7e-4516-a289-b9ddf45b7c81">IsRoleDefinition</a>


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

<a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>


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

<a href="https://msdn.microsoft.com/b05fd157-6526-49d6-9bb1-fcf8c59cc74e">Operations</a>


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

<a href="https://msdn.microsoft.com/a4baa899-78eb-4a3b-bcc1-0b8c2831b10f">Tasks</a>


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

<a href="https://msdn.microsoft.com/68f31203-00de-4729-a836-51d5dc8c8091">Writable</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the task can be modified by the user context that initialized it.

</td>
</tr>
</table> 

