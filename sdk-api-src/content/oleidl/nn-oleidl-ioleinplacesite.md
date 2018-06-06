---
UID: NN:oleidl.IOleInPlaceSite
title: IOleInPlaceSite
author: windows-sdk-content
description: Manages the interaction between the container and the object's in-place client site. Recall that the client site is the display site for embedded objects, and provides position and conceptual information about the object.
old-location: com\ioleinplacesite.htm
old-project: com
ms.assetid: 6d37e022-8c19-48b3-affb-e0eca19b5e05
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IOleInPlaceSite, IOleInPlaceSite interface [COM], IOleInPlaceSite interface [COM],described, _ole_ioleinplacesite, com.ioleinplacesite, oleidl/IOleInPlaceSite
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: USERCLASSTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleInPlaceSite
product: Windows
targetos: Windows
req.lib: 
req.dll: Adhocreportingexcelclient.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOleInPlaceSite interface


## -description


Manages the interaction between the container and the object's in-place client site. Recall that the client site is the display site for embedded objects, and provides position and conceptual information about the object.

This interface provides methods that manage in-place objects. With <b>IOleInPlaceSite</b>, you can determine if an object can be activated and manage its activation and deactivation. You can notify the container when one of its objects is being activated and inform the container that a composite menu will replace the container's regular menu. It provides methods that make it possible for the in-place object to retrieve the window object hierarchy, and the position in the parent window where the object should place its in-place activation window. Finally, it determines how the container scrolls the object, manages the object undo state, and notifies the object when its borders have changed.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleInPlaceSite</b> interface inherits from <a href="https://msdn.microsoft.com/2d0efbae-4a1c-43b1-9021-8d89377f7282">IOleWindow</a>. <b>IOleInPlaceSite</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOleInPlaceSite</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac960359-7e02-43b6-ac42-0000af15b1a4">CanInPlaceActivate</a>
</td>
<td align="left" width="63%">
Determines whether the container can activate the object in place.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59229720-cd3b-45d5-90c4-391acb124f4d">DeactivateAndUndo</a>
</td>
<td align="left" width="63%">
Deactivates the object, ends the in-place session, and reverts to the container's saved undo state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8fe69aa5-a526-4e95-920b-01f84ae4ca83">DiscardUndoState</a>
</td>
<td align="left" width="63%">
Instructs the container to discard its undo state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f6cf62b3-5a64-49aa-b0bd-56744ecee313">GetWindowContext</a>
</td>
<td align="left" width="63%">
Enables an in-place object to retrieve the window interfaces that form the window object hierarchy, and the position in the parent window where the object's in-place activation window should be located.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5744911-1ea6-4482-988d-8def16229f4c">OnInPlaceActivate</a>
</td>
<td align="left" width="63%">
Notifies the container that one of its objects is being activated in place.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/070aac4e-94b6-4e23-b132-1dc833774c8b">OnInPlaceDeactivate</a>
</td>
<td align="left" width="63%">
Notifies the container that it should reinstall its user interface and take focus, and whether the object has an undoable state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a12d6a2a-6581-41e3-b33d-74af5d772e71">OnPosRectChange</a>
</td>
<td align="left" width="63%">
Notifies the container that the object extents have changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d863805c-58c1-4e35-84b5-72f01a4ba205">OnUIActivate</a>
</td>
<td align="left" width="63%">
Notifies the container that the object is about to be activated in place and that the object is going to replace the container's main menu with an in-place composite menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/926c02b4-0bfa-4509-b5bc-4e5007e4db1a">OnUIDeactivate</a>
</td>
<td align="left" width="63%">
Notifies the container to reinstall its user interface and take focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a169c4c6-b600-4812-bf71-d7fcd7486ff1">Scroll</a>
</td>
<td align="left" width="63%">
Instructs the container to scroll the view of the object by the specified number of pixels.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/dafee149-926a-4d08-a43d-5847682db645">IOleClientSite</a>



<a href="https://msdn.microsoft.com/2d0efbae-4a1c-43b1-9021-8d89377f7282">IOleWindow</a>
 

 

