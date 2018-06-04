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

# tagSCROLLBARINFO structure


## -description


The <b>SCROLLBARINFO</b> structure contains scroll bar information.


## -struct-fields




### -field cbSize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Specifies the size, in bytes, of the structure. Before calling the <a href="https://msdn.microsoft.com/949e9d33-35d6-4f27-a1c7-7b034ac52e6d">GetScrollBarInfo</a> function, set <b>cbSize</b> to <b>sizeof</b>(<b>SCROLLBARINFO</b>). 


### -field rcScrollBar

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a></b>

Coordinates of the scroll bar as specified in a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure.


### -field dxyLineButton

Type: <b>int</b>

Height or width of the thumb. 


### -field xyThumbTop

Type: <b>int</b>

Position of the top or left of the thumb. 


### -field xyThumbBottom

Type: <b>int</b>

Position of the bottom or right of the thumb. 


### -field reserved

Type: <b>int</b>

Reserved. 


### -field rgstate

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a>[CCHILDREN_SCROLLBAR+1]</b>

An array of <b>DWORD</b> elements. Each element indicates the state of a scroll bar component. The following values show the scroll bar component that corresponds to each array index.
					

<table class="clsStd">
<tr>
<th>Index</th>
<th>Scroll bar component</th>
</tr>
<tr>
<td>0</td>
<td>The scroll bar itself.</td>
</tr>
<tr>
<td>1</td>
<td>The top or right arrow button.</td>
</tr>
<tr>
<td>2</td>
<td>The page up or page right region.</td>
</tr>
<tr>
<td>3</td>
<td>The scroll box (thumb).</td>
</tr>
<tr>
<td>4</td>
<td>The page down or page left region.</td>
</tr>
<tr>
<td>5</td>
<td>The bottom or left arrow button.</td>
</tr>
</table>
 

The <b>DWORD</b> element for each scroll bar component can include a combination of the following bit flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="STATE_SYSTEM_INVISIBLE"></a><a id="state_system_invisible"></a><dl>
<dt><b>STATE_SYSTEM_INVISIBLE</b></dt>
</dl>
</td>
<td width="60%">
For the scroll bar itself, indicates the specified vertical or horizontal scroll bar does not exist. For the page up or page down regions, indicates the thumb is positioned such that the region does not exist.

</td>
</tr>
<tr>
<td width="40%"><a id="STATE_SYSTEM_OFFSCREEN"></a><a id="state_system_offscreen"></a><dl>
<dt><b>STATE_SYSTEM_OFFSCREEN</b></dt>
</dl>
</td>
<td width="60%">
For the scroll bar itself, indicates the window is sized such that the specified vertical or horizontal scroll bar is not currently displayed.

</td>
</tr>
<tr>
<td width="40%"><a id="STATE_SYSTEM_PRESSED"></a><a id="state_system_pressed"></a><dl>
<dt><b>STATE_SYSTEM_PRESSED</b></dt>
</dl>
</td>
<td width="60%">
The arrow button or page region is pressed.

</td>
</tr>
<tr>
<td width="40%"><a id="STATE_SYSTEM_UNAVAILABLE"></a><a id="state_system_unavailable"></a><dl>
<dt><b>STATE_SYSTEM_UNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The component is disabled.

</td>
</tr>
</table>
 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/949e9d33-35d6-4f27-a1c7-7b034ac52e6d">GetScrollBarInfo</a>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/23a21f01-b22c-4f4c-a6c0-43c9b2d80ebb">Scroll Bars</a>
 

 

