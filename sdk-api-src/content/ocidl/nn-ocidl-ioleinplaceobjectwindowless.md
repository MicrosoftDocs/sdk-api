---
UID: NN:ocidl.IOleInPlaceObjectWindowless
title: IOleInPlaceObjectWindowless (ocidl.h)
description: Enables a windowless object to process window messages and participate in drag and drop operations. It is derived from and extends the IOleInPlaceObject interface.helpviewer_keywords: ["IOleInPlaceObjectWindowless","IOleInPlaceObjectWindowless interface [COM]","IOleInPlaceObjectWindowless interface [COM]","described","_ole_ioleinplaceobjectwindowless","com.ioleinplaceobjectwindowless","ocidl/IOleInPlaceObjectWindowless"]
old-location: com\ioleinplaceobjectwindowless.htm
tech.root: com
ms.assetid: 86aabb46-6bc7-4953-b4eb-8692552ca380
ms.date: 12/05/2018
ms.keywords: IOleInPlaceObjectWindowless, IOleInPlaceObjectWindowless interface [COM], IOleInPlaceObjectWindowless interface [COM],described, _ole_ioleinplaceobjectwindowless, com.ioleinplaceobjectwindowless, ocidl/IOleInPlaceObjectWindowless
f1_keywords:
- ocidl/IOleInPlaceObjectWindowless
dev_langs:
- c++
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
- OCIdl.h
api_name:
- IOleInPlaceObjectWindowless
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOleInPlaceObjectWindowless interface


## -description


Enables a windowless object to process window messages and participate in drag and drop operations. It is derived from and extends the <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceobject">IOleInPlaceObject</a> interface.

A small object, such as a control, does not need a window of its own. Instead, it can rely on its container to dispatch window messages and help the object to participate in drag and drop operations. The container must implement the <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ioleinplacesitewindowless">IOleInPlaceSiteWindowless</a> interface. Otherwise, the object must act as a normal compound document object and create a window when it is activated.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleInPlaceObjectWindowless</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceobject">IOleInPlaceObject</a>. <b>IOleInPlaceObjectWindowless</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOleInPlaceObjectWindowless</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ioleinplaceobjectwindowless-getdroptarget">GetDropTarget</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a> interface for an in-place active, windowless object that supports drag and drop.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ioleinplaceobjectwindowless-onwindowmessage">OnWindowMessage</a>
</td>
<td align="left" width="63%">
Dispatches a message from a container to a windowless object that is in-place active.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceobject">IOleInPlaceObject</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ioleinplacesitewindowless">IOleInPlaceSiteWindowless</a>
 

 

