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

# IPrintManagerInterop interface


## -description


Enables access to <a href="https://msdn.microsoft.com/81ad3b9b-36f2-46c0-8315-1d2bdfcebe75">PrintManager</a> methods in a Windows Store app that manages multiple windows.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPrintManagerInterop</b> interface inherits from <b>IInspectable</b>. <b>IPrintManagerInterop</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPrintManagerInterop</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8cbf37b6-6756-4399-aa6b-01eb63c8c6db">GetForWindow</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/81ad3b9b-36f2-46c0-8315-1d2bdfcebe75">PrintManager</a> instance for the specified window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2414279e-e1ef-48c7-87a1-a09ad367aec4">ShowPrintUIForWindowAsync</a>
</td>
<td align="left" width="63%">
Displays the UI for printing content for the specified window.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/81ad3b9b-36f2-46c0-8315-1d2bdfcebe75">PrintManager</a>
 

 

