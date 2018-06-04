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

# DrawCaption function


## -description


The <b>DrawCaption</b> function draws a window caption.


## -parameters




### -param hwnd [in]

A handle to a window that supplies text and an icon for the window caption.


### -param hdc [in]

A handle to a device context. The function draws the window caption into this device context.


### -param lprect

TBD


### -param flags

TBD




#### - lprc [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that specifies the bounding rectangle for the window caption in logical coordinates.


#### - uFlags [in]

The drawing options. This parameter can be zero or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DC_ACTIVE"></a><a id="dc_active"></a><dl>
<dt><b>DC_ACTIVE</b></dt>
</dl>
</td>
<td width="60%">
The function uses the colors that denote an active caption.

</td>
</tr>
<tr>
<td width="40%"><a id="DC_BUTTONS"></a><a id="dc_buttons"></a><dl>
<dt><b>DC_BUTTONS</b></dt>
</dl>
</td>
<td width="60%">

                 If set, the function draws the buttons in the caption bar (to minimize, restore, or close an application).

</td>
</tr>
<tr>
<td width="40%"><a id="DC_GRADIENT"></a><a id="dc_gradient"></a><dl>
<dt><b>DC_GRADIENT</b></dt>
</dl>
</td>
<td width="60%">

                 When this flag is set, the function uses COLOR_GRADIENTACTIVECAPTION (if the DC_ACTIVE flag was set) or COLOR_GRADIENTINACTIVECAPTION for the title-bar color.

If this flag is not set, the function uses COLOR_ACTIVECAPTION or COLOR_INACTIVECAPTION for both colors.

</td>
</tr>
<tr>
<td width="40%"><a id="DC_ICON"></a><a id="dc_icon"></a><dl>
<dt><b>DC_ICON</b></dt>
</dl>
</td>
<td width="60%">
The function draws the icon when drawing the caption text.

</td>
</tr>
<tr>
<td width="40%"><a id="DC_INBUTTON"></a><a id="dc_inbutton"></a><dl>
<dt><b>DC_INBUTTON</b></dt>
</dl>
</td>
<td width="60%">
The function draws the caption as a button.

</td>
</tr>
<tr>
<td width="40%"><a id="DC_SMALLCAP"></a><a id="dc_smallcap"></a><dl>
<dt><b>DC_SMALLCAP</b></dt>
</dl>
</td>
<td width="60%">
The function draws a small caption, using the current small caption font.

</td>
</tr>
<tr>
<td width="40%"><a id="DC_TEXT"></a><a id="dc_text"></a><dl>
<dt><b>DC_TEXT</b></dt>
</dl>
</td>
<td width="60%">
The function draws the caption text when drawing the caption.

</td>
</tr>
</table>
 

If DC_SMALLCAP is specified, the function draws a normal window caption.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -see-also




<a href="https://msdn.microsoft.com/ec18323e-c13b-4328-83bf-9e4ed4a712b8">Painting and Drawing Functions</a>



<a href="https://msdn.microsoft.com/8e6034af-4dea-4579-b476-52f6dd3d5bc7">Painting and Drawing Overview</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>
 

 

