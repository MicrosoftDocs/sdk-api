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

# ITfMouseSink::OnMouseEvent


## -description




## -parameters




### -param uEdge [in]

Contains the offset, in characters, of the mouse position from the start of the range of text. For more information, see the Remarks section.


### -param uQuadrant [in]

Contains the zero-based quadrant index, relative to the edge, that the mouse position lies in. For more information, see the Remarks section.


### -param dwBtnStatus [in]

Indicates the mouse button state at the time of the event. See the <i>wParam</i> parameter of the <a href="_win32_wm_mousemove">WM_MOUSEMOVE</a> message for possible values.


### -param pfEaten [out]

Pointer to a BOOL that, on exit, indicates if the mouse event was handled. If this value receives <b>TRUE</b>, the mouse event was handled. If this value is <b>FALSE</b>, the mouse event was not handled.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
</table>
 




## -remarks



The caller should translate double-click events into multiple mouse button down events. This enables a text service to detect double-click events even if the context window does not support double-clicks.

<i>uEdge</i> contains the offset, in characters, of the mouse position from the start of the text range. The mouse position is always rounded to the closest edge. Each edge is divided into four equal quadrants with two quadrants preceding the edge and two quadrants following the edge. <i>uQuadrant</i> contains the zero-based quadrant index of the mouse position. In the figure below, point "X" is in quadrant 2 of edge 1 and point "Y" is in quadrant 1 of edge 3.

<img alt="Quadrant relationship to edge of a range of text" border="border" src="images/mousedge.gif"/>



## -see-also




<a href="https://msdn.microsoft.com/d6e5549e-768d-47af-a553-84430641cda4">ITfMouseSink</a>



<a href="https://msdn.microsoft.com/d73b2b9b-8904-4507-9b32-dcb8946fb887">ITfMouseTracker::AdviseMouseSink
      </a>



<a href="https://msdn.microsoft.com/365538cd-0f18-45ce-91c2-ee3255b7fa93">
        ITfMouseTrackerACP::AdviseMouseSink
      </a>



<a href="_win32_wm_mousemove">WM_MOUSEMOVE</a>
 

 

