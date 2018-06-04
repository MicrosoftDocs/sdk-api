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

# TBMETRICS structure


## -description


Defines the metrics of a toolbar that are used to shrink or expand toolbar items.


## -struct-fields




### -field cbSize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Size of the <b>TBMETRICS</b> structure.


### -field dwMask

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Mask that determines the metric to retrieve. It can be any combination of the following:



<table class="clsStd">
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>TBMF_PAD</td>
<td>Retrieve the <b>cxPad</b> and <b>cyPad</b> values.</td>
</tr>
<tr>
<td>TBMF_BARPAD</td>
<td>Retrieve the <b>cxBarPad</b> and <b>cyBarPad</b> values.</td>
</tr>
<tr>
<td>TBMF_BUTTONSPACING</td>
<td>Retrieve the <b>cxButtonSpacing</b> and <b>cyButtonSpacing</b> values.</td>
</tr>
</table>
 




### -field cxPad

Type: <b>int</b>

Width of the padding inside the toolbar buttons, between the content and the edge of the button.


### -field cyPad

Type: <b>int</b>

Height of the padding inside the toolbar buttons, between the content and the edge of the button.


### -field cxBarPad

Type: <b>int</b>

Width of the toolbar. Not used.


### -field cyBarPad

Type: <b>int</b>

Height of the toolbar. Not used.


### -field cxButtonSpacing

Type: <b>int</b>

Width of the space between toolbar buttons.


### -field cyButtonSpacing

Type: <b>int</b>

Height of the space between toolbar buttons.


## -remarks



The metrics specified by <b>TBMETRICS</b> structure are used to size the non-animating buttons on a toolbar. Button can shrink or expand so that all visible items fit on the window.

The padding values are used to create a blank area between the edge of the button and the button's image and/or text. Where and how much padding is actually applied depends on the type of the button and whether it has an image. The horizontal padding is applied to both the right and left of the button, and the vertical padding is applied to both the top and bottom of the button. Padding is only applied to buttons that have the <a href="Toolbar_Control_and_Button_Styles.htm">TBSTYLE_AUTOSIZE</a> style.

Although values for <b>cxBarPad</b> and <b>cyBarPad</b> can be set and retrieved they currently have no effect and are not used.



