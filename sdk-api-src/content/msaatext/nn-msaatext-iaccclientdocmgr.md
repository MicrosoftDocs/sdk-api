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

# IAccClientDocMgr interface


## -description


<p class="CCE_Message">[Active Accessibility Text Services is deprecated. Please see     
<a href="http://go.microsoft.com/fwlink/p/?linkid=131573">Microsoft Windows Text Services Framework</a>
for more information on advanced text input and natural language technologies.
		]

Exposes methods for client applications to retrieve documents.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAccClientDocMgr</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAccClientDocMgr</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAccClientDocMgr</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/490a202b-1fb4-4f2e-a8f2-f9134a8a9daf">GetDocuments</a>
</td>
<td align="left" width="63%">
Retrieves a list of documents that have been registered with the Microsoft Active Accessibility run time. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/102a511b-43ad-48c1-8953-647482fa452b">GetFocused</a>
</td>
<td align="left" width="63%">
Retrieves the document that has focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb67c208-b79b-4219-ba5b-2235ae4a1dcf">LookupByHWND</a>
</td>
<td align="left" width="63%">
Retrieves a document from an HWND.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6de40049-3c61-458c-b7e0-c4b416780581">LookupByPoint</a>
</td>
<td align="left" width="63%">
Retrieves a document from a point on the screen.

</td>
</tr>
</table> 

