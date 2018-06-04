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

# IPlayToManagerInterop interface


## -description


Enables access to <a href="https://msdn.microsoft.com/e5de08a6-cc89-4422-bfe7-f170b8ec4412">PlayToManager</a> methods in a Windows Store app that manages multiple windows.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPlayToManagerInterop</b> interface inherits from <b>IInspectable</b>. <b>IPlayToManagerInterop</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPlayToManagerInterop</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/444f0d68-a6ae-46de-aa97-d7d505c95948">GetForWindow</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/e5de08a6-cc89-4422-bfe7-f170b8ec4412">PlayToManager</a> instance for the specified window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/106ddd95-06dd-479a-8350-39d791add469">ShowPlayToUIForWindow</a>
</td>
<td align="left" width="63%">
Displays the Play To UI for the specified window.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/e5de08a6-cc89-4422-bfe7-f170b8ec4412">PlayToManager</a>
 

 

