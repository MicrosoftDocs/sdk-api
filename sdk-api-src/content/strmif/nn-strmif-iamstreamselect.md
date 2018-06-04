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

# IAMStreamSelect interface


## -description



The <code>IAMStreamSelect</code> interface selects from the available streams on a parser filter. For example, a file might contain audio streams encoded in several languages, such as English, German, and French. The application could use this interface to select which language is played.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMStreamSelect</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMStreamSelect</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMStreamSelect</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of available streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451004">Enable</a>
</td>
<td align="left" width="63%">
Enables or disables a given stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9396d4fb-e06e-4b54-9601-fd443c81ff35">Info</a>
</td>
<td align="left" width="63%">
Retrieves information about a given stream.

</td>
</tr>
</table> 


## -remarks



The following filters implement this interface:

<ul>
<li>
<a href="https://msdn.microsoft.com/abadf37f-2876-496d-90e7-77c3475a0064">MPEG-1 Stream Splitter</a> filter</li>
<li>
<a href="https://msdn.microsoft.com/06704a5a-e7ae-4187-ae36-32512d951aaf">MPEG-2 Splitter</a> filter</li>
<li>
<a href="https://msdn.microsoft.com/9b09dd86-3c22-4565-82a0-106d5ca2e42d">SAMI (CC) Parser</a> filter</li>
</ul>


