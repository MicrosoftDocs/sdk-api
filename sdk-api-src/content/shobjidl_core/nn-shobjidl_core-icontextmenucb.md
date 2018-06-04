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

# IContextMenuCB interface


## -description


Exposes a method that enables the callback of a context menu. For example, to add a shield icon to a <b>menuItem</b> that requires elevation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IContextMenuCB</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IContextMenuCB</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IContextMenuCB</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d091b1a-26b5-4cab-a3ec-6d59dc7d103e">CallBack</a>
</td>
<td align="left" width="63%">
Enables the callback function for a context menu.

</td>
</tr>
</table> 


## -remarks



This is the callback interface specified in the <a href="https://msdn.microsoft.com/007861f6-1e66-4c5f-a459-3cfbe9f8cec2">DEFCONTEXTMENU</a> structure passed with the function <a href="https://msdn.microsoft.com/055ff0a0-9ba7-463d-9684-3fd072b190da">SHCreateDefaultContextMenu</a>.

This interface enables <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> implementations to manage context menu messages before, after, and during the context menu handling of these messages.



