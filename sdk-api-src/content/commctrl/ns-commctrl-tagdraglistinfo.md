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

# tagDRAGLISTINFO structure


## -description


Contains information about a drag event. The pointer to <b>DRAGLISTINFO</b> is passed as the 
			<i>lParam</i> parameter of the drag list message. 


## -struct-fields




### -field uNotification

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The notification code that specifies the type of drag event. This member can be one of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DL_BEGINDRAG"></a><a id="dl_begindrag"></a><dl>
<dt><b>DL_BEGINDRAG</b></dt>
</dl>
</td>
<td width="60%">
The user has clicked the left mouse button on a list item.

</td>
</tr>
<tr>
<td width="40%"><a id="DL_CANCELDRAG"></a><a id="dl_canceldrag"></a><dl>
<dt><b>DL_CANCELDRAG</b></dt>
</dl>
</td>
<td width="60%">
The user has canceled the drag operation by clicking the right mouse button or pressing the ESC key.

</td>
</tr>
<tr>
<td width="40%"><a id="DL_DRAGGING"></a><a id="dl_dragging"></a><dl>
<dt><b>DL_DRAGGING</b></dt>
</dl>
</td>
<td width="60%">
The user has moved the mouse while dragging an item. 

</td>
</tr>
<tr>
<td width="40%"><a id="DL_DROPPED"></a><a id="dl_dropped"></a><dl>
<dt><b>DL_DROPPED</b></dt>
</dl>
</td>
<td width="60%">
The user has released the left mouse button, completing a drag operation.

</td>
</tr>
</table>
 


### -field hWnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the drag list box. 


### -field ptCursor

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a></b>

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structure that contains the current x- and y-coordinates of the mouse cursor. 

