---
UID: NS:commctrl.BUTTON_IMAGELIST
title: BUTTON_IMAGELIST (commctrl.h)
description: Contains information about an image list that is used with a button control.
helpviewer_keywords: ["*PBUTTON_IMAGELIST","BUTTON_IMAGELIST","BUTTON_IMAGELIST structure [Windows Controls]","BUTTON_IMAGELIST_ALIGN_BOTTOM","BUTTON_IMAGELIST_ALIGN_CENTER","BUTTON_IMAGELIST_ALIGN_LEFT","BUTTON_IMAGELIST_ALIGN_RIGHT","BUTTON_IMAGELIST_ALIGN_TOP","PBUTTON_IMAGELIST","PBUTTON_IMAGELIST structure pointer [Windows Controls]","_win32_BUTTON_IMAGELIST_str","_win32_BUTTON_IMAGELIST_str_cpp","commctrl/BUTTON_IMAGELIST","commctrl/PBUTTON_IMAGELIST","controls.BUTTON_IMAGELIST","controls._win32_BUTTON_IMAGELIST_str"]
old-location: controls\BUTTON_IMAGELIST.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonstructures\button_imagelist.htm
ms.date: 12/05/2018
ms.keywords: '*PBUTTON_IMAGELIST, BUTTON_IMAGELIST, BUTTON_IMAGELIST structure [Windows Controls], BUTTON_IMAGELIST_ALIGN_BOTTOM, BUTTON_IMAGELIST_ALIGN_CENTER, BUTTON_IMAGELIST_ALIGN_LEFT, BUTTON_IMAGELIST_ALIGN_RIGHT, BUTTON_IMAGELIST_ALIGN_TOP, PBUTTON_IMAGELIST, PBUTTON_IMAGELIST structure pointer [Windows Controls], _win32_BUTTON_IMAGELIST_str, _win32_BUTTON_IMAGELIST_str_cpp, commctrl/BUTTON_IMAGELIST, commctrl/PBUTTON_IMAGELIST, controls.BUTTON_IMAGELIST, controls._win32_BUTTON_IMAGELIST_str'
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
req.typenames: BUTTON_IMAGELIST, *PBUTTON_IMAGELIST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PBUTTON_IMAGELIST
 - commctrl/PBUTTON_IMAGELIST
 - BUTTON_IMAGELIST
 - commctrl/BUTTON_IMAGELIST
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
 - BUTTON_IMAGELIST
---

# BUTTON_IMAGELIST structure


## -description

Contains information about an image list that is used with a button control.

## -struct-fields

### -field himl

Type: <b>HIMAGELIST</b>

A handle to the image list. The provider retains ownership of the image list and is ultimately responsible for its disposal. Under Windows Vista, you can pass BCCL_NOGLYPH in this parameter to indicate that no glyph should be displayed.

### -field margin

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>

A <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> that specifies the margin around the icon.

### -field uAlign

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A <b>UINT</b> that specifies the alignment to use. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BUTTON_IMAGELIST_ALIGN_LEFT"></a><a id="button_imagelist_align_left"></a><dl>
<dt><b>BUTTON_IMAGELIST_ALIGN_LEFT</b></dt>
</dl>
</td>
<td width="60%">
Align the image with the left margin.

</td>
</tr>
<tr>
<td width="40%"><a id="BUTTON_IMAGELIST_ALIGN_RIGHT"></a><a id="button_imagelist_align_right"></a><dl>
<dt><b>BUTTON_IMAGELIST_ALIGN_RIGHT</b></dt>
</dl>
</td>
<td width="60%">
Align the image with the right margin.

</td>
</tr>
<tr>
<td width="40%"><a id="BUTTON_IMAGELIST_ALIGN_TOP"></a><a id="button_imagelist_align_top"></a><dl>
<dt><b>BUTTON_IMAGELIST_ALIGN_TOP</b></dt>
</dl>
</td>
<td width="60%">
Align the image with the top margin

</td>
</tr>
<tr>
<td width="40%"><a id="BUTTON_IMAGELIST_ALIGN_BOTTOM"></a><a id="button_imagelist_align_bottom"></a><dl>
<dt><b>BUTTON_IMAGELIST_ALIGN_BOTTOM</b></dt>
</dl>
</td>
<td width="60%">
Align the image with the bottom margin

</td>
</tr>
<tr>
<td width="40%"><a id="BUTTON_IMAGELIST_ALIGN_CENTER"></a><a id="button_imagelist_align_center"></a><dl>
<dt><b>BUTTON_IMAGELIST_ALIGN_CENTER</b></dt>
</dl>
</td>
<td width="60%">
Center the image.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/Controls/bcm-getimagelist">BCM_GETIMAGELIST</a>



<a href="/windows/desktop/Controls/bcm-setimagelist">BCM_SETIMAGELIST</a>



<a href="/windows/desktop/api/commctrl/nf-commctrl-button_getimagelist">Button_GetImageList</a>



<a href="/windows/desktop/api/commctrl/nf-commctrl-button_setimagelist">Button_SetImageList</a>



<a href="/windows/desktop/Controls/buttons">Buttons</a>



<b>Conceptual</b>



<b>Reference</b>

