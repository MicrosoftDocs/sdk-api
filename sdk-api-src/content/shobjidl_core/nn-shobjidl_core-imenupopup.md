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

# IMenuPopup interface


## -description


<p class="CCE_Message">[<b>IMenuPopup</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Exposes methods to navigate through a shortcut menu.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMenuPopup</b> interface inherits from <a href="https://msdn.microsoft.com/78b9666b-f913-4745-975e-f8dd6e9f89b4">IDeskBar</a>. <b>IMenuPopup</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMenuPopup</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/972e8a08-e1ce-4bd2-b602-20b7b1acb71f">OnSelect</a>
</td>
<td align="left" width="63%">
Handles selection notifications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f889955-9c6d-4b6c-ae04-389d2bff3bd9">Popup</a>
</td>
<td align="left" width="63%">
Invokes the shortcut menu at a specified onscreen location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c2f80502-bac5-4a6f-95ba-1610c548e636">SetSubMenu</a>
</td>
<td align="left" width="63%">
Sets the given menu bar interface to be the submenu of the calling application object's interface.

</td>
</tr>
</table> 

