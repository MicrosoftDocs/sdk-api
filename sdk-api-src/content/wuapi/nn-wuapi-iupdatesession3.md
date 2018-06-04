---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IUpdateSession3 interface


## -description


Represents a session in which the caller can perform operations that involve updates. For example, this interface represents sessions in which the caller performs a search, download, installation, or uninstallation operation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUpdateSession3</b> interface inherits from <a href="https://msdn.microsoft.com/c074cbc8-6d1b-41dd-a54c-30f02fca9215">IUpdateSession2</a>. <b>IUpdateSession3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUpdateSession3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/79d8f489-5375-48e2-a40d-d6f38f4843aa">CreateUpdateServiceManager</a>
</td>
<td align="left" width="63%">
Returns a pointer to an <a href="https://msdn.microsoft.com/26b75edc-eb43-4ee0-8040-da8b3252cf21">IUpdateServiceManager2</a> interface for the session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/614a392e-949b-4fba-a4e7-5c393c2b51c3">QueryHistory</a>
</td>
<td align="left" width="63%">
Returns a pointer to an <a href="https://msdn.microsoft.com/c3bc764b-c9cc-4567-963e-2e481bdda611">IUpdateHistoryEntryCollection</a> interface. The interface contains matching event records on the computer. This causes the <a href="https://msdn.microsoft.com/614a392e-949b-4fba-a4e7-5c393c2b51c3">QueryHistory</a> method to synchronously query the computer for the history of update events.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/c074cbc8-6d1b-41dd-a54c-30f02fca9215">IUpdateSession2</a>
 

 

