---
UID: NN:oleidl.IOleWindow
title: IOleWindow (oleidl.h)
author: windows-sdk-content
description: The IOleWindow interface provides methods that allow an application to obtain the handle to the various windows that participate in in-place activation, and also to enter and exit context-sensitive help mode.
old-location: com\iolewindow.htm
tech.root: com
ms.assetid: 2d0efbae-4a1c-43b1-9021-8d89377f7282
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOleWindow, IOleWindow interface [COM], IOleWindow interface [COM],described, _ole_iolewindow, com.iolewindow, oleidl/IOleWindow
ms.topic: interface
f1_keywords: 
 - "oleidl/IOleWindow"
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
 - IOleWindow
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOleWindow interface


## -description


The <b>IOleWindow</b> interface provides methods that allow an application to obtain the handle to the various windows that participate in in-place activation, and also to enter and exit context-sensitive help mode.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleWindow</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOleWindow</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOleWindow</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-iolewindow-contextsensitivehelp">ContextSensitiveHelp</a>
</td>
<td align="left" width="63%">
Determines whether context-sensitive help mode should be entered during an in-place activation session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-iolewindow-getwindow">GetWindow</a>
</td>
<td align="left" width="63%">
Retrieves a handle to one of the windows participating in in-place activation (frame, document, parent, or in-place object window).

</td>
</tr>
</table> 


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
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceobject">IOleInPlaceObject</a>
</td>
<td>
Implemented by objects and used by an object's immediate container to activate and deactivate the object.

</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceactiveobject">IOleInPlaceActiveObject</a>
</td>
<td>
Implemented by objects and used by the top-level container to manipulate the object while it is active. Provides a direct channel of communication between an active object and its frame and document windows.

</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceuiwindow">IOleInPlaceUIWindow</a>
</td>
<td>
Implemented by containers and used by objects to manipulate the container's document window.

</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceframe">IOleInPlaceFrame</a>
</td>
<td>
Implemented by containers and used by objects to control the container's frame window.

</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-ioleinplacesite">IOleInPlaceSite</a>
</td>
<td>
Implemented by containers and used by objects to interact with the in-place client site.

</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ioleinplacesiteex">IOleInPlaceSiteEx</a>
</td>
<td>
Implemented by containers and called by objects to optimize activation and deactivation.

</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ioleinplacesitewindowless">IOleInPlaceSiteWindowless</a>
</td>
<td>
Implemented by containers and called by windowless object to obtain services from its container.

</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ioleinplaceobjectwindowless">IOleInPlaceObjectWindowless</a>
</td>
<td>
Implemented by windowless objects called by containers to support window message processing and drag and drop operations for windowless objects.

</td>
</tr>
</table>
 

These interfaces can be arranged in three hierarchical levels with various interfaces implemented at each level. Calls that install user-interface menus commands and frame adornments, activate and switch between windows, and dispatch menu and keystrokes take place between the top-level container and the active object. Calls that support activating, deactivating, scrolling, or clipping span the containment hierarchy, with each level performing the correct actions.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ole2/nf-ole2-olecreatemenudescriptor">OleCreateMenuDescriptor</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ole2/nf-ole2-oledestroymenudescriptor">OleDestroyMenuDescriptor</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ole2/nf-ole2-oletranslateaccelerator">OleTranslateAccelerator</a>
 

 

