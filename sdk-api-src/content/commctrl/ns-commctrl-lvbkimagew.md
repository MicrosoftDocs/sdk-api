---
UID: NS:commctrl.tagLVBKIMAGEW
title: LVBKIMAGEW (commctrl.h)
description: Contains information about the background image of a list-view control. This structure is used for both setting and retrieving background image information. (Unicode)
helpviewer_keywords: ["*LPLVBKIMAGEW","LPLVBKIMAGE","LPLVBKIMAGE structure pointer [Windows Controls]","LVBKIF_FLAG_ALPHABLEND","LVBKIF_FLAG_TILEOFFSET","LVBKIF_SOURCE_HBITMAP","LVBKIF_SOURCE_NONE","LVBKIF_SOURCE_URL","LVBKIF_STYLE_NORMAL","LVBKIF_STYLE_TILE","LVBKIF_TYPE_WATERMARK","LVBKIMAGE","LVBKIMAGE structure [Windows Controls]","LVBKIMAGEA","LVBKIMAGEW","_win32_LVBKIMAGE","_win32_LVBKIMAGE_cpp","commctrl/LPLVBKIMAGE","commctrl/LVBKIMAGE","commctrl/LVBKIMAGEA","commctrl/LVBKIMAGEW","controls.LVBKIMAGE","controls._win32_LVBKIMAGE"]
old-location: controls\LVBKIMAGE.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\structures\lvbkimage.htm
ms.date: 12/05/2018
ms.keywords: '*LPLVBKIMAGEW, LPLVBKIMAGE, LPLVBKIMAGE structure pointer [Windows Controls], LVBKIF_FLAG_ALPHABLEND, LVBKIF_FLAG_TILEOFFSET, LVBKIF_SOURCE_HBITMAP, LVBKIF_SOURCE_NONE, LVBKIF_SOURCE_URL, LVBKIF_STYLE_NORMAL, LVBKIF_STYLE_TILE, LVBKIF_TYPE_WATERMARK, LVBKIMAGE, LVBKIMAGE structure [Windows Controls], LVBKIMAGEA, LVBKIMAGEW, _win32_LVBKIMAGE, _win32_LVBKIMAGE_cpp, commctrl/LPLVBKIMAGE, commctrl/LVBKIMAGE, commctrl/LVBKIMAGEA, commctrl/LVBKIMAGEW, controls.LVBKIMAGE, controls._win32_LVBKIMAGE'
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LVBKIMAGEW (Unicode) and LVBKIMAGEA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: LVBKIMAGEW, *LPLVBKIMAGEW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagLVBKIMAGEW
 - commctrl/tagLVBKIMAGEW
 - LPLVBKIMAGEW
 - commctrl/LPLVBKIMAGEW
 - LVBKIMAGEW
 - commctrl/LVBKIMAGEW
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
 - LVBKIMAGE
 - LVBKIMAGEA
 - LVBKIMAGEW
---

# LVBKIMAGEW structure


## -description

Contains information about the background image of a list-view control. This structure is used for both setting and retrieving background image information.

## -struct-fields

### -field ulFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">ULONG</a></b>

This member may be one or more of the following flags. You can use the LVBKIF_SOURCE_MASK value to mask off all but the source flags. You can use the LVBKIF_STYLE_MASK value to mask off all but the style flags. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LVBKIF_SOURCE_NONE"></a><a id="lvbkif_source_none"></a><dl>
<dt><b>LVBKIF_SOURCE_NONE</b></dt>
</dl>
</td>
<td width="60%">
The list-view control has no background image. 

</td>
</tr>
<tr>
<td width="40%"><a id="LVBKIF_SOURCE_HBITMAP"></a><a id="lvbkif_source_hbitmap"></a><dl>
<dt><b>LVBKIF_SOURCE_HBITMAP</b></dt>
</dl>
</td>
<td width="60%">
A background bitmap is supplied via the <b>hbm</b> member of <b>LVBKIMAGE</b>.  If the message <a href="/windows/desktop/Controls/lvm-setbkimage">LVM_SETBKIMAGE</a> succeeds, then the list-view takes ownership of the bitmap.

</td>
</tr>
<tr>
<td width="40%"><a id="LVBKIF_SOURCE_URL"></a><a id="lvbkif_source_url"></a><dl>
<dt><b>LVBKIF_SOURCE_URL</b></dt>
</dl>
</td>
<td width="60%">
The <b>pszImage</b> member contains the URL of the background image. 

</td>
</tr>
<tr>
<td width="40%"><a id="LVBKIF_STYLE_NORMAL"></a><a id="lvbkif_style_normal"></a><dl>
<dt><b>LVBKIF_STYLE_NORMAL</b></dt>
</dl>
</td>
<td width="60%">
The background image is displayed normally. 

</td>
</tr>
<tr>
<td width="40%"><a id="LVBKIF_STYLE_TILE"></a><a id="lvbkif_style_tile"></a><dl>
<dt><b>LVBKIF_STYLE_TILE</b></dt>
</dl>
</td>
<td width="60%">
The background image will be tiled to fill the entire background of the control.

</td>
</tr>
<tr>
<td width="40%"><a id="LVBKIF_FLAG_TILEOFFSET"></a><a id="lvbkif_flag_tileoffset"></a><dl>
<dt><b>LVBKIF_FLAG_TILEOFFSET</b></dt>
</dl>
</td>
<td width="60%">
Specify the coordinates of the first tile. This flag is valid only if the <b>LVBKIF_STYLE_TILE</b> flag is also specified. If this flag is not specified, the first tile begins at the upper-left corner of the client area. If you use ComCtl32.dll <a href="/windows/desktop/Controls/common-control-versions"> Version 6.0 </a> the <b>xOffsetPercent</b> and <b>yOffsetPercent</b> fields contain pixels, not percentage values, to specify the coordinates of the first tile. Comctl32.dll version 6 is not redistributable but it is included in Windows or later. Also, you must specify Comctl32.dll version 6 in a manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="LVBKIF_TYPE_WATERMARK"></a><a id="lvbkif_type_watermark"></a><dl>
<dt><b>LVBKIF_TYPE_WATERMARK</b></dt>
</dl>
</td>
<td width="60%">
A watermark background bitmap is supplied via the <b>hbm</b> member of <b>LVBKIMAGE</b>. If the <a href="/windows/desktop/Controls/lvm-setbkimage">LVM_SETBKIMAGE</a> message succeeds, then the list-view control takes ownership of the bitmap.

</td>
</tr>
<tr>
<td width="40%"><a id="LVBKIF_FLAG_ALPHABLEND"></a><a id="lvbkif_flag_alphablend"></a><dl>
<dt><b>LVBKIF_FLAG_ALPHABLEND</b></dt>
</dl>
</td>
<td width="60%">
Valid only when LVBKIF_TYPE_WATERMARK is also specified.  This flag indicates the bitmap provided via LVBKIF_TYPE_WATERMARK contains a valid alpha channel.

</td>
</tr>
</table>

### -field hbm

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HBITMAP</a></b>

The handle of the background bitmap. This member is valid only if the 
					<b>LVBKIF_SOURCE_HBITMAP</b> flag is set in 
					<b>ulFlags</b>.

### -field pszImage

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPTSTR</a></b>

Address of a NULL-terminated string that contains the URL of the background image. This member is valid only if the 
					<b>LVBKIF_SOURCE_URL</b> flag is set in 
					<b>ulFlags</b>. This member must be initialized to point to the buffer that contains or receives the text before sending the message.

### -field cchImageMax

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Size of the buffer at the address in 
					<b>pszImage</b>. If information is being sent to the control, this member is ignored.

### -field xOffsetPercent

Type: <b>int</b>

Percentage of the control's client area that the image should be offset horizontally. For example, at 0 percent, the image will be displayed against the left edge of the control's client area. At 50 percent, the image will be displayed horizontally centered in the control's client area. At 100 percent, the image will be displayed against the right edge of the control's client area. This member is valid only when 
					<b>LVBKIF_STYLE_NORMAL</b> is specified in 
					<b>ulFlags</b>. If both <b>LVBKIF_FLAG_TILEOFFSET</b> and <b>LVBKIF_STYLE_TILE</b> are specified in <b>ulFlags</b>, then the value specifies the pixel, not percentage offset, of the first tile. Otherwise, the value is ignored.

### -field yOffsetPercent

Type: <b>int</b>

Percentage of the control's client area that the image should be offset vertically. For example, at 0 percent, the image will be displayed against the top edge of the control's client area. At 50 percent, the image will be displayed vertically centered in the control's client area. At 100 percent, the image will be displayed against the bottom edge of the control's client area. This member is valid only when 
					<b>LVBKIF_STYLE_NORMAL</b> is specified in 
					<b>ulFlags</b>. If both <b>LVBKIF_FLAG_TILEOFFSET</b> and <b>LVBKIF_STYLE_TILE</b> are specified in <b>ulFlags</b>, then the value specifies the pixel, not percentage offset, of the first tile. Otherwise, the value is ignored.

## -remarks

This structure is used with the <a href="/windows/desktop/Controls/lvm-getbkimage">LVM_GETBKIMAGE</a> and <a href="/windows/desktop/Controls/lvm-setbkimage">LVM_SETBKIMAGE</a> messages. 




> [!NOTE]
> The commctrl.h header defines LVBKIMAGE as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
