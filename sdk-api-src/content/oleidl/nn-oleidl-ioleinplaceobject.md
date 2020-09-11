---
UID: NN:oleidl.IOleInPlaceObject
title: IOleInPlaceObject (oleidl.h)
description: Manages the activation and deactivation of in-place objects, and determines how much of the in-place object should be visible.
helpviewer_keywords: ["IOleInPlaceObject","IOleInPlaceObject interface [COM]","IOleInPlaceObject interface [COM]","described","_ole_ioleinplaceobject","com.ioleinplaceobject","oleidl/IOleInPlaceObject"]
old-location: com\ioleinplaceobject.htm
tech.root: com
ms.assetid: c14de79d-e844-49cf-ae70-6c3e417fab90
ms.date: 12/05/2018
ms.keywords: IOleInPlaceObject, IOleInPlaceObject interface [COM], IOleInPlaceObject interface [COM],described, _ole_ioleinplaceobject, com.ioleinplaceobject, oleidl/IOleInPlaceObject
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOleInPlaceObject
 - oleidl/IOleInPlaceObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleInPlaceObject
---

# IOleInPlaceObject interface


## -description

Manages the activation and deactivation of in-place objects, and determines how much of the in-place object should be visible.

You can obtain a pointer to <b>IOleInPlaceObject</b> by calling <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> on <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleInPlaceObject</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-iolewindow">IOleWindow</a>. <b>IOleInPlaceObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOleInPlaceObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceobject-inplacedeactivate">InPlaceDeactivate</a>
</td>
<td align="left" width="63%">
Deactivates an active in-place object and discards the object's undo state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceobject-reactivateandundo">ReactivateAndUndo</a>
</td>
<td align="left" width="63%">
Reactivates a previously deactivated object, undoing the last state of the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceobject-setobjectrects">SetObjectRects</a>
</td>
<td align="left" width="63%">
Specifies how much of the in-place object is to be visible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceobject-uideactivate">UIDeactivate</a>
</td>
<td align="left" width="63%">
Deactivates and removes the user interface of an active in-place object.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-iolewindow">IOleWindow</a>

