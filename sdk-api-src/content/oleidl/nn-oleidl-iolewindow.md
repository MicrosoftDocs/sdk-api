---
UID: NN:oleidl.IOleWindow
title: IOleWindow (oleidl.h)
description: The IOleWindow interface provides methods that allow an application to obtain the handle to the various windows that participate in in-place activation, and also to enter and exit context-sensitive help mode.
helpviewer_keywords: ["IOleWindow","IOleWindow interface [COM]","IOleWindow interface [COM]","described","_ole_iolewindow","com.iolewindow","oleidl/IOleWindow"]
old-location: com\iolewindow.htm
tech.root: com
ms.assetid: 2d0efbae-4a1c-43b1-9021-8d89377f7282
ms.date: 12/05/2018
ms.keywords: IOleWindow, IOleWindow interface [COM], IOleWindow interface [COM],described, _ole_iolewindow, com.iolewindow, oleidl/IOleWindow
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
 - IOleWindow
 - oleidl/IOleWindow
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
 - IOleWindow
---

# IOleWindow interface


## -description

The <b>IOleWindow</b> interface provides methods that allow an application to obtain the handle to the various windows that participate in in-place activation, and also to enter and exit context-sensitive help mode.

## -inheritance

The <b>IOleWindow</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOleWindow</b> also has these types of members:

## -remarks

Several other in-place activation interfaces are derived from the <b>IOleWindow</b> interface. Containers and objects must implement and use these interfaces in order to support in-place activation. The following table briefly summarizes each of these interfaces.

<table>
<tr>
<th>Interface</th>
<th>Description</th>
</tr>
<tr>
<td><b>IOleWindow</b></td>
<td>
The base interface. Implemented and used by containers and objects to obtain window handles and manage context-sensitive help. This interface is not supported for use across machine boundaries.

</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceobject">IOleInPlaceObject</a>
</td>
<td>
Implemented by objects and used by an object's immediate container to activate and deactivate the object.

</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceactiveobject">IOleInPlaceActiveObject</a>
</td>
<td>
Implemented by objects and used by the top-level container to manipulate the object while it is active. Provides a direct channel of communication between an active object and its frame and document windows.

</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceuiwindow">IOleInPlaceUIWindow</a>
</td>
<td>
Implemented by containers and used by objects to manipulate the container's document window.

</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceframe">IOleInPlaceFrame</a>
</td>
<td>
Implemented by containers and used by objects to control the container's frame window.

</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplacesite">IOleInPlaceSite</a>
</td>
<td>
Implemented by containers and used by objects to interact with the in-place client site.

</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleinplacesiteex">IOleInPlaceSiteEx</a>
</td>
<td>
Implemented by containers and called by objects to optimize activation and deactivation.

</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleinplacesitewindowless">IOleInPlaceSiteWindowless</a>
</td>
<td>
Implemented by containers and called by windowless object to obtain services from its container.

</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleinplaceobjectwindowless">IOleInPlaceObjectWindowless</a>
</td>
<td>
Implemented by windowless objects called by containers to support window message processing and drag and drop operations for windowless objects.

</td>
</tr>
</table>
 

These interfaces can be arranged in three hierarchical levels with various interfaces implemented at each level. Calls that install user-interface menus commands and frame adornments, activate and switch between windows, and dispatch menu and keystrokes take place between the top-level container and the active object. Calls that support activating, deactivating, scrolling, or clipping span the containment hierarchy, with each level performing the correct actions.

## -see-also

<a href="/windows/desktop/api/ole2/nf-ole2-olecreatemenudescriptor">OleCreateMenuDescriptor</a>



<a href="/windows/desktop/api/ole2/nf-ole2-oledestroymenudescriptor">OleDestroyMenuDescriptor</a>



<a href="/windows/desktop/api/ole2/nf-ole2-oletranslateaccelerator">OleTranslateAccelerator</a>
