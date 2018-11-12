---
UID: NN:azroles.IAzTasks
title: IAzTasks
author: windows-sdk-content
description: Represents a collection of IAzTask objects.
old-location: security\iaztasks.htm
tech.root: secauthz
ms.assetid: 324dec16-3fd6-4289-ba15-002e8626dec8
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IAzTasks, IAzTasks interface [Security], IAzTasks interface [Security],described, azroles/IAzTasks, security.iaztasks
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
 - IAzTasks
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzTasks interface


## -description


The <b>IAzTasks</b> interface represents a collection of  
<a href="https://msdn.microsoft.com/en-us/library/Aa378367(v=VS.85).aspx">IAzTask</a> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzTasks</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IAzTasks</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IAzTasks</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2598295f-da23-4eb2-aefc-e8e43f8c0f60">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/2598295f-da23-4eb2-aefc-e8e43f8c0f60">_NewEnum</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/505768ce-27a3-4f36-aeea-081cf8e45d14">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/505768ce-27a3-4f36-aeea-081cf8e45d14">Count</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eddfebba-4f0e-405a-90b5-dbdc87dca3da">get_Item</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/en-us/library/Aa378372(v=VS.85).aspx">Item</a> property.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzTasks</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2598295f-da23-4eb2-aefc-e8e43f8c0f60">_NewEnum</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/en-us/library/ms221053(v=VS.85).aspx">IEnumVARIANT</a> interface on an object that can be used to enumerate the collection. This property is hidden within Visual Basic and Visual Basic Scripting Edition (VBScript).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/505768ce-27a3-4f36-aeea-081cf8e45d14">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the number of <a href="https://msdn.microsoft.com/en-us/library/Aa378367(v=VS.85).aspx">IAzTask</a> objects in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa378372(v=VS.85).aspx">Item</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/en-us/library/Aa378367(v=VS.85).aspx">IAzTask</a> object at the specified index into the <b>IAzTasks</b> collection.

</td>
</tr>
</table> 

