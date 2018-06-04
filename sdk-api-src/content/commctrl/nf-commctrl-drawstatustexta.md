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

# DrawStatusTextA function


## -description


The <b>DrawStatusText</b> function draws the specified text in the style of a status window with borders.


## -parameters




### -param hDC

TBD


### -param lprc

Type: <b>LPCRECT</b>

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that contains the position, in client coordinates, of the rectangle in which the text is drawn. The function draws the borders just inside the edges of the specified rectangle. 


### -param pszText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCTSTR</a></b>

Pointer to a null-terminated string that specifies the text to display. Tab characters in the string determine whether the string is left-aligned, right-aligned, or centered. 


### -param uFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Text drawing flags. This parameter can be a combination of these values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SBT_NOBORDERS"></a><a id="sbt_noborders"></a><dl>
<dt><b>SBT_NOBORDERS</b></dt>
</dl>
</td>
<td width="60%">
Prevents borders from being drawn around the specified text.

</td>
</tr>
<tr>
<td width="40%"><a id="SBT_POPOUT"></a><a id="sbt_popout"></a><dl>
<dt><b>SBT_POPOUT</b></dt>
</dl>
</td>
<td width="60%">
Draws highlighted borders that make the text stand out.

</td>
</tr>
<tr>
<td width="40%"><a id="SBT_RTLREADING"></a><a id="sbt_rtlreading"></a><dl>
<dt><b>SBT_RTLREADING</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the string pointed to by 
						<i>pszText</i> will be displayed in the opposite direction to the text in the parent window. 

</td>
</tr>
</table>
 


#### - hdc

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a></b>

Handle to the display context for the window. 


## -returns



This function does not return a value.




## -remarks



Normal windows display text left-to-right (LTR). Windows can be <i>mirrored</i> to display languages such as Hebrew or Arabic that read right-to-left (RTL). Normally, the <i>pszText</i> string will be displayed in the same direction as the text in its parent window. If SBT_RTLREADING is set, the <i>pszText</i> string will read in the opposite direction from the text in the parent window.



