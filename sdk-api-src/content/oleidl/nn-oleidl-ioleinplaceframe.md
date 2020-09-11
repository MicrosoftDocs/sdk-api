---
UID: NN:oleidl.IOleInPlaceFrame
title: IOleInPlaceFrame (oleidl.h)
description: Controls the container's top-level frame window.
helpviewer_keywords: ["IOleInPlaceFrame","IOleInPlaceFrame interface [COM]","IOleInPlaceFrame interface [COM]","described","_ole_ioleinplaceframe","com.ioleinplaceframe","oleidl/IOleInPlaceFrame"]
old-location: com\ioleinplaceframe.htm
tech.root: com
ms.assetid: c530aff7-fd83-413d-8945-0c9d1bfb51ba
ms.date: 12/05/2018
ms.keywords: IOleInPlaceFrame, IOleInPlaceFrame interface [COM], IOleInPlaceFrame interface [COM],described, _ole_ioleinplaceframe, com.ioleinplaceframe, oleidl/IOleInPlaceFrame
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
 - IOleInPlaceFrame
 - oleidl/IOleInPlaceFrame
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
 - IOleInPlaceFrame
---

# IOleInPlaceFrame interface


## -description

Controls the container's top-level frame window. This control involves allowing the container to insert its menu group into the composite menu, install the composite menu into the appropriate window frame, and remove the container's menu elements from the composite menu. It sets and displays status text relevant to the in-place object. It also enables or disables the frame's modeless dialog boxes, and translates accelerator keystrokes intended for the container's frame.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleInPlaceFrame</b> interface inherits from <b>IOleInPlaceUIWindow</b>. <b>IOleInPlaceFrame</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOleInPlaceFrame</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceframe-enablemodeless">EnableModeless</a>
</td>
<td align="left" width="63%">
Enables or disables a frame's modeless dialog boxes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceframe-insertmenus">InsertMenus</a>
</td>
<td align="left" width="63%">
Enables the container to insert menu groups.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceframe-removemenus">RemoveMenus</a>
</td>
<td align="left" width="63%">
Removes a container's menu elements from the composite menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceframe-setmenu">SetMenu</a>
</td>
<td align="left" width="63%">
Adds a composite menu to the window frame containing the object being activated in place.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceframe-setstatustext">SetStatusText</a>
</td>
<td align="left" width="63%">
Sets and displays status text about the in-place object in the container's frame window status line.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceframe-translateaccelerator">TranslateAccelerator</a>
</td>
<td align="left" width="63%">
Translates accelerator keystrokes intended for the container's frame while an object is active in place.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceuiwindow">IOleInPlaceUIWindow</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-iolewindow">IOleWindow</a>

