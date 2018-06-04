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

# IDropSourceNotify interface


## -description


The <b>IDropSourceNotify</b> interface is implemented on an <a href="https://msdn.microsoft.com/963a36bc-4ad7-4591-bffc-a96b4310177d">IDropSource</a> object to receive notifications from OLE when a user drags the mouse into or out of a potential drop target window.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDropSourceNotify</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IDropSourceNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDropSourceNotify</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f2ca860-1f63-4cc1-9a9e-4efb6fceb867">DragEnterTarget</a>
</td>
<td align="left" width="63%">
OLE calls this method when the user drags the mouse cursor into a potential drop target window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6267db46-92ce-43b8-8e3f-ffd7d2b8a2e8">DragLeaveTarget</a>
</td>
<td align="left" width="63%">
OLE calls this method when the user drags the mouse cursor out of a potential drop target window.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/963a36bc-4ad7-4591-bffc-a96b4310177d">IDropSource</a>



<a href="https://msdn.microsoft.com/13fbe834-1ef8-4944-b2e4-9f5c413c65c8">IDropTarget</a>
 

 

