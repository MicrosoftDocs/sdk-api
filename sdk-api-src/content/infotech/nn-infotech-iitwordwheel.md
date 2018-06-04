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

# IITWordWheel interface


## -description


Use this interface to perform word wheel keyword lookups. The <b>Lookup</b> method offers several ways of performing a search: it returns either an exact match, or the closest approximation based on a given prefix.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IITWordWheel</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IITWordWheel</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IITWordWheel</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a>
</td>
<td align="left" width="63%">
Closes a word wheel.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a>
</td>
<td align="left" width="63%">
Returns the number of entries in a word wheel.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3276511f-c7c2-40ce-9502-8804d3777da2">Lookup(,IITResultSet,)</a>
</td>
<td align="left" width="63%">
Looks up an entry and returns contents as a result set.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d4275bc2-a623-46c0-88e2-b2951fa0232e">Lookup(,LPVOID,DWORD)</a>
</td>
<td align="left" width="63%">
Looks up an entry and returns contents in a buffer.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9242a7dd-83d4-4d30-8285-721778800744">Lookup(LPCVOID,BOOL,)</a>
</td>
<td align="left" width="63%">
Returns the word wheel entry that is closest to the specified prefix.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a>
</td>
<td align="left" width="63%">
Opens a word wheel.



</td>
</tr>
</table> 

