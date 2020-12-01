---
UID: NS:commctrl.tagLVGROUPMETRICS
title: LVGROUPMETRICS (commctrl.h)
description: Contains information about the display of groups in a list-view control.
helpviewer_keywords: ["*PLVGROUPMETRICS","LVGROUPMETRICS","LVGROUPMETRICS structure [Windows Controls]","PLVGROUPMETRICS","PLVGROUPMETRICS structure pointer [Windows Controls]","commctrl/LVGROUPMETRICS","commctrl/PLVGROUPMETRICS","controls.LVGROUPMETRICS","controls.inet_LVGROUPMETRICS","inet_LVGROUPMETRICS","inet_LVGROUPMETRICS_cpp"]
old-location: controls\LVGROUPMETRICS.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\structures\lvgroupmetrics.htm
ms.date: 12/05/2018
ms.keywords: '*PLVGROUPMETRICS, LVGROUPMETRICS, LVGROUPMETRICS structure [Windows Controls], PLVGROUPMETRICS, PLVGROUPMETRICS structure pointer [Windows Controls], commctrl/LVGROUPMETRICS, commctrl/PLVGROUPMETRICS, controls.LVGROUPMETRICS, controls.inet_LVGROUPMETRICS, inet_LVGROUPMETRICS, inet_LVGROUPMETRICS_cpp'
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
req.typenames: LVGROUPMETRICS, *PLVGROUPMETRICS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagLVGROUPMETRICS
 - commctrl/tagLVGROUPMETRICS
 - PLVGROUPMETRICS
 - commctrl/PLVGROUPMETRICS
 - LVGROUPMETRICS
 - commctrl/LVGROUPMETRICS
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
 - LVGROUPMETRICS
---

# LVGROUPMETRICS structure


## -description

Contains information about the display of groups in a list-view control.

## -struct-fields

### -field cbSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Size of the <b>LVGROUPMETRICS</b> structure.

### -field mask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Flags that specify which members contain or are to receive valid data. Can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVGMF_BORDERCOLOR</dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVGMF_BORDERSIZE</dt>
</dl>
</td>
<td width="60%">
The <b>Left</b>, <b>Top</b>, <b>Right</b>, and <b>Bottom</b> members are valid.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVGMF_NONE</dt>
</dl>
</td>
<td width="60%">
No members are valid.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVGMF_TEXTCOLOR</dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
</table>

### -field Left

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Specifies the width of the left border in icon, small icon, or tile view.

### -field Top

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Specifies the width of the top border in all group views.

### -field Right

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Specifies the width of the right border in icon, small icon, or tile view.

### -field Bottom

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Specifies the width of the bottom border in all group views.

### -field crLeft

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>

Specifies the color of the left border. Not implemented.

### -field crTop

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>

Specifies the color of the top border. Not implemented.

### -field crRight

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>

Specifies the color of the right border. Not implemented.

### -field crBottom

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>

Specifies the color of the bottom border. Not implemented.

### -field crHeader

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>

Specifies the color of the header text. Not implemented.

### -field crFooter

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>

Specifies the color of the footer text. Not implemented.

## -remarks

The width of a border determines the margins of the area within which items are placed. The top border is highlighted when the user moves the cursor over it, and when the user clicks on this border in a list that allows multiple selection, all items in the group are selected.

## -see-also

<a href="/windows/desktop/Controls/lvm-getgroupmetrics">LVM_GETGROUPMETRICS</a>



<a href="/windows/desktop/Controls/lvm-setgroupmetrics">LVM_SETGROUPMETRICS</a>



<a href="/windows/desktop/api/commctrl/nf-commctrl-listview_getgroupmetrics">ListView_GetGroupMetrics</a>



<a href="/windows/desktop/api/commctrl/nf-commctrl-listview_setgroupmetrics">ListView_SetGroupMetrics</a>



<b>Reference</b>