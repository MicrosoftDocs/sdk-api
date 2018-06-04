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

# tagCURSORINFO structure


## -description


Contains global cursor information.


## -struct-fields




### -field cbSize

Type: <b>DWORD</b>

The size of the structure, in bytes. The caller must set this to <code>sizeof(CURSORINFO)</code>.


### -field flags

Type: <b>DWORD</b>

The cursor state. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The cursor is hidden.

</td>
</tr>
<tr>
<td width="40%"><a id="CURSOR_SHOWING"></a><a id="cursor_showing"></a><dl>
<dt><b>CURSOR_SHOWING</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The cursor is showing.

</td>
</tr>
<tr>
<td width="40%"><a id="CURSOR_SUPPRESSED"></a><a id="cursor_suppressed"></a><dl>
<dt><b>CURSOR_SUPPRESSED</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
<b>Windows 8</b>: The cursor is suppressed. This flag indicates that the system is not drawing the cursor because the user is providing input through touch or pen instead of the mouse.

</td>
</tr>
</table>
 


### -field hCursor

Type: <b>HCURSOR</b>

A handle to the cursor. 


### -field ptScreenPos

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a></b>

A   structure that receives the screen coordinates of the cursor.


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/d24e21f2-224d-4f32-aa0b-70844e3628ad">Cursors</a>



<a href="https://msdn.microsoft.com/4dea42e7-f78f-4e34-9e1d-e76123a209fc">GetCursorInfo</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a>



<b>Reference</b>
 

 

