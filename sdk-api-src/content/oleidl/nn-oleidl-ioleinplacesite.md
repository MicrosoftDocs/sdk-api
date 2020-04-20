---
UID: NN:oleidl.IOleInPlaceSite
title: IOleInPlaceSite (oleidl.h)
description: Manages the interaction between the container and the object's in-place client site. Recall that the client site is the display site for embedded objects, and provides position and conceptual information about the object.helpviewer_keywords: ["IOleInPlaceSite","IOleInPlaceSite interface [COM]","IOleInPlaceSite interface [COM]","described","_ole_ioleinplacesite","com.ioleinplacesite","oleidl/IOleInPlaceSite"]
old-location: com\ioleinplacesite.htm
tech.root: com
ms.assetid: 6d37e022-8c19-48b3-affb-e0eca19b5e05
ms.date: 12/05/2018
ms.keywords: IOleInPlaceSite, IOleInPlaceSite interface [COM], IOleInPlaceSite interface [COM],described, _ole_ioleinplacesite, com.ioleinplacesite, oleidl/IOleInPlaceSite
f1_keywords:
- oleidl/IOleInPlaceSite
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- OleIdl.h
api_name:
- IOleInPlaceSite
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOleInPlaceSite interface


## -description


Manages the interaction between the container and the object's in-place client site. Recall that the client site is the display site for embedded objects, and provides position and conceptual information about the object.

This interface provides methods that manage in-place objects. With <b>IOleInPlaceSite</b>, you can determine if an object can be activated and manage its activation and deactivation. You can notify the container when one of its objects is being activated and inform the container that a composite menu will replace the container's regular menu. It provides methods that make it possible for the in-place object to retrieve the window object hierarchy, and the position in the parent window where the object should place its in-place activation window. Finally, it determines how the container scrolls the object, manages the object undo state, and notifies the object when its borders have changed.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleInPlaceSite</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-iolewindow">IOleWindow</a>. <b>IOleInPlaceSite</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleinplacesite-caninplaceactivate">CanInPlaceActivate</a>
</td>
<td align="left" width="63%">
Determines whether the container can activate the object in place.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleinplacesite-deactivateandundo">DeactivateAndUndo</a>
</td>
<td align="left" width="63%">
Deactivates the object, ends the in-place session, and reverts to the container's saved undo state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleinplacesite-discardundostate">DiscardUndoState</a>
</td>
<td align="left" width="63%">
Instructs the container to discard its undo state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleinplacesite-getwindowcontext">GetWindowContext</a>
</td>
<td align="left" width="63%">
Enables an in-place object to retrieve the window interfaces that form the window object hierarchy, and the position in the parent window where the object's in-place activation window should be located.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleinplacesite-oninplaceactivate">OnInPlaceActivate</a>
</td>
<td align="left" width="63%">
Notifies the container that one of its objects is being activated in place.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleinplacesite-oninplacedeactivate">OnInPlaceDeactivate</a>
</td>
<td align="left" width="63%">
Notifies the container that it should reinstall its user interface and take focus, and whether the object has an undoable state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleinplacesite-onposrectchange">OnPosRectChange</a>
</td>
<td align="left" width="63%">
Notifies the container that the object extents have changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleinplacesite-onuiactivate">OnUIActivate</a>
</td>
<td align="left" width="63%">
Notifies the container that the object is about to be activated in place and that the object is going to replace the container's main menu with an in-place composite menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleinplacesite-onuideactivate">OnUIDeactivate</a>
</td>
<td align="left" width="63%">
Notifies the container to reinstall its user interface and take focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleinplacesite-scroll">Scroll</a>
</td>
<td align="left" width="63%">
Instructs the container to scroll the view of the object by the specified number of pixels.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-ioleclientsite">IOleClientSite</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-iolewindow">IOleWindow</a>
 

 

