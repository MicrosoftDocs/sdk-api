---
UID: NN:azroles.IAzOperation
title: IAzOperation
author: windows-sdk-content
description: Defines a low-level operation supported by an application.
old-location: security\iazoperation.htm
tech.root: SecAuthZ
ms.assetid: 054fa4aa-70be-4618-a635-3941c830ea4e
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IAzOperation, IAzOperation interface [Security], IAzOperation interface [Security],described, azroles/IAzOperation, security.iazoperation
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzOperation
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzOperation interface


## -description


The <b>IAzOperation</b> interface defines a low-level operation supported by an application.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzOperation</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IAzOperation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IAzOperation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/211def10-d696-4b23-b54c-21f1f9b8f7ff">GetProperty</a>
</td>
<td align="left" width="63%">
Returns the <b>IAzOperation</b> object property  with the specified property ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f510fdb4-922d-488c-ad3d-3468da6a2fb6">SetProperty</a>
</td>
<td align="left" width="63%">
Sets the specified value to the <b>IAzOperation</b> object property  with the specified property ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f6265bfa-c856-47db-a688-f5de25ef7157">Submit</a>
</td>
<td align="left" width="63%">
Persists changes made to the <b>IAzOperation</b> object.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzOperation</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d4d22aae-6ca3-4a97-aa44-fa07674dc556">ApplicationData</a>


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

<a href="https://msdn.microsoft.com/9f39032d-7624-43f8-91a4-6e616e691156">Description</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a comment that describes the operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e1ebacda-513c-49f7-bb36-15229fdb0b3b">Name</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the name of the operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3466dea1-b005-40fc-87d1-29b5e033f6a0">OperationID</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves an application-specific value that uniquely identifies the operation  within the application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/16745237-23d9-4818-b8f8-de93405ae9ac">Writable</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the operation can be modified by the  user context that initialized it.

</td>
</tr>
</table> 

