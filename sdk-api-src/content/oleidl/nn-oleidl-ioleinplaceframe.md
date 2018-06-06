---
UID: NN:oleidl.IOleInPlaceFrame
title: IOleInPlaceFrame
author: windows-sdk-content
description: Controls the container's top-level frame window.
old-location: com\ioleinplaceframe.htm
old-project: com
ms.assetid: c530aff7-fd83-413d-8945-0c9d1bfb51ba
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IOleInPlaceFrame, IOleInPlaceFrame interface [COM], IOleInPlaceFrame interface [COM],described, _ole_ioleinplaceframe, com.ioleinplaceframe, oleidl/IOleInPlaceFrame
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
 - IOleInPlaceFrame
product: Windows
targetos: Windows
req.lib: 
req.dll: Adhocreportingexcelclient.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
<a href="https://msdn.microsoft.com/4c6ea1ee-861d-45ff-a9d2-d3b241f00c9f">EnableModeless</a>
</td>
<td align="left" width="63%">
Enables or disables a frame's modeless dialog boxes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/659ea109-c2c1-4146-aed2-60b1ce853d89">InsertMenus</a>
</td>
<td align="left" width="63%">
Enables the container to insert menu groups.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92d9fcda-8ede-4f38-ad56-59c4a75fe45a">RemoveMenus</a>
</td>
<td align="left" width="63%">
Removes a container's menu elements from the composite menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dc26a399-846d-4d15-b406-752350e528c2">SetMenu</a>
</td>
<td align="left" width="63%">
Adds a composite menu to the window frame containing the object being activated in place.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e857bdbe-5510-4e35-ba73-d52b239e5b77">SetStatusText</a>
</td>
<td align="left" width="63%">
Sets and displays status text about the in-place object in the container's frame window status line.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f755b919-b810-4b66-b3c2-bf38bd525d60">TranslateAccelerator</a>
</td>
<td align="left" width="63%">
Translates accelerator keystrokes intended for the container's frame while an object is active in place.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3cfb31aa-9746-438c-af64-8236c170fe88">IOleInPlaceUIWindow</a>



<a href="https://msdn.microsoft.com/2d0efbae-4a1c-43b1-9021-8d89377f7282">IOleWindow</a>
 

 

