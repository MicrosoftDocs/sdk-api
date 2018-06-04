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

# IOleInPlaceUIWindow interface


## -description


Implemented by container applications and used by object applications to negotiate border space on the document or frame window. The container provides a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure in which the object can place toolbars and other similar controls, determines if tools can in fact be installed around the object's window frame, allocates space for the border, and establishes a communication channel between the object and each frame and document window.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleInPlaceUIWindow</b> interface inherits from <a href="https://msdn.microsoft.com/2d0efbae-4a1c-43b1-9021-8d89377f7282">IOleWindow</a>. <b>IOleInPlaceUIWindow</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOleInPlaceUIWindow</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ee9970a-b937-4538-b3b8-460647086db1">GetBorder</a>
</td>
<td align="left" width="63%">
Retrieves the outer rectange for toolbars and controls while the object is active in place.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd477b1d-e9a5-4b99-adf1-8e62de975730">RequestBorderSpace</a>
</td>
<td align="left" width="63%">
Determines whether there is space available for tools to be installed around object's window frame while the object is active in place.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ed1b09a-44e4-41dc-aa35-27efb3df66d6">SetActiveObject</a>
</td>
<td align="left" width="63%">
Provides a direct channel of communication between the object and each of the frame and document windows.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c806a02-db6d-444e-a049-22c4ae2b19b0">SetBorderSpace</a>
</td>
<td align="left" width="63%">
Allocates space for the border requested in the call to <a href="https://msdn.microsoft.com/fd477b1d-e9a5-4b99-adf1-8e62de975730">RequestBorderSpace</a>.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/2d0efbae-4a1c-43b1-9021-8d89377f7282">IOleWindow</a>
 

 

