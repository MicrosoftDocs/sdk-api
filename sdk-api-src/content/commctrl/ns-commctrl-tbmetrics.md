---
UID: NS:commctrl.TBMETRICS
title: TBMETRICS (commctrl.h)
description: Defines the metrics of a toolbar that are used to shrink or expand toolbar items.
helpviewer_keywords: ["*LPTBMETRICS","LPTBMETRICS","LPTBMETRICS structure pointer [Windows Controls]","TBMETRICS","TBMETRICS structure [Windows Controls]","commctrl/LPTBMETRICS","commctrl/TBMETRICS","controls.TBMETRICS","controls.inet_TBMETRICS","inet_TBMETRICS","inet_TBMETRICS_cpp"]
old-location: controls\TBMETRICS.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\toolbar\structures\tbmetrics.htm
ms.date: 12/05/2018
ms.keywords: '*LPTBMETRICS, LPTBMETRICS, LPTBMETRICS structure pointer [Windows Controls], TBMETRICS, TBMETRICS structure [Windows Controls], commctrl/LPTBMETRICS, commctrl/TBMETRICS, controls.TBMETRICS, controls.inet_TBMETRICS, inet_TBMETRICS, inet_TBMETRICS_cpp'
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TBMETRICS, *LPTBMETRICS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPTBMETRICS
 - commctrl/LPTBMETRICS
 - TBMETRICS
 - commctrl/TBMETRICS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - TBMETRICS
---

# TBMETRICS structure


## -description

Defines the metrics of a toolbar that are used to shrink or expand toolbar items.

## -struct-fields

### -field cbSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Size of the <b>TBMETRICS</b> structure.

### -field dwMask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

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

The padding values are used to create a blank area between the edge of the button and the button's image and/or text. Where and how much padding is actually applied depends on the type of the button and whether it has an image. The horizontal padding is applied to both the right and left of the button, and the vertical padding is applied to both the top and bottom of the button. Padding is only applied to buttons that have the <a href="/windows/desktop/Controls/toolbar-control-and-button-styles">TBSTYLE_AUTOSIZE</a> style.

Although values for <b>cxBarPad</b> and <b>cyBarPad</b> can be set and retrieved they currently have no effect and are not used.

