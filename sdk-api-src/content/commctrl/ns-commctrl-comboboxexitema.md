---
UID: NS:commctrl.tagCOMBOBOXEXITEMA
title: COMBOBOXEXITEMA (commctrl.h)
description: Contains information about an item in a ComboBoxEx control. (ANSI)
helpviewer_keywords: ["*PCOMBOBOXEXITEMA","CBEIF_DI_SETITEM","CBEIF_IMAGE","CBEIF_INDENT","CBEIF_LPARAM","CBEIF_OVERLAY","CBEIF_SELECTEDIMAGE","CBEIF_TEXT","COMBOBOXEXITEM","COMBOBOXEXITEM structure [Windows Controls]","COMBOBOXEXITEMA","COMBOBOXEXITEMW","PCOMBOBOXEXITEM","PCOMBOBOXEXITEM structure pointer [Windows Controls]","_win32_COMBOBOXEXITEM","_win32_COMBOBOXEXITEM_cpp","commctrl/COMBOBOXEXITEM","commctrl/COMBOBOXEXITEMA","commctrl/COMBOBOXEXITEMW","commctrl/PCOMBOBOXEXITEM","controls.COMBOBOXEXITEM","controls._win32_COMBOBOXEXITEM"]
old-location: controls\COMBOBOXEXITEM.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboex\structures\comboboxexitem.htm
ms.date: 12/05/2018
ms.keywords: '*PCOMBOBOXEXITEMA, CBEIF_DI_SETITEM, CBEIF_IMAGE, CBEIF_INDENT, CBEIF_LPARAM, CBEIF_OVERLAY, CBEIF_SELECTEDIMAGE, CBEIF_TEXT, COMBOBOXEXITEM, COMBOBOXEXITEM structure [Windows Controls], COMBOBOXEXITEMA, COMBOBOXEXITEMW, PCOMBOBOXEXITEM, PCOMBOBOXEXITEM structure pointer [Windows Controls], _win32_COMBOBOXEXITEM, _win32_COMBOBOXEXITEM_cpp, commctrl/COMBOBOXEXITEM, commctrl/COMBOBOXEXITEMA, commctrl/COMBOBOXEXITEMW, commctrl/PCOMBOBOXEXITEM, controls.COMBOBOXEXITEM, controls._win32_COMBOBOXEXITEM'
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: COMBOBOXEXITEMW (Unicode) and COMBOBOXEXITEMA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: COMBOBOXEXITEMA, *PCOMBOBOXEXITEMA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCOMBOBOXEXITEMA
 - commctrl/tagCOMBOBOXEXITEMA
 - PCOMBOBOXEXITEMA
 - commctrl/PCOMBOBOXEXITEMA
 - COMBOBOXEXITEMA
 - commctrl/COMBOBOXEXITEMA
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
 - COMBOBOXEXITEM
 - COMBOBOXEXITEMA
 - COMBOBOXEXITEMW
---

# COMBOBOXEXITEMA structure


## -description

Contains information about an item in a ComboBoxEx control.

## -struct-fields

### -field mask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A set of bit flags that specify attributes of this structure or of an operation that is using this structure. The flags specify members that are valid or must be filled in. This member can be a combination of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CBEIF_DI_SETITEM"></a><a id="cbeif_di_setitem"></a><dl>
<dt><b>CBEIF_DI_SETITEM</b></dt>
</dl>
</td>
<td width="60%">
Set this flag when processing <a href="/windows/desktop/Controls/cben-getdispinfo">CBEN_GETDISPINFO</a>; the ComboBoxEx control will retain the supplied information and will not request it again.

</td>
</tr>
<tr>
<td width="40%"><a id="CBEIF_IMAGE"></a><a id="cbeif_image"></a><dl>
<dt><b>CBEIF_IMAGE</b></dt>
</dl>
</td>
<td width="60%">
The 
						<b>iImage</b> member is valid or must be filled in.

</td>
</tr>
<tr>
<td width="40%"><a id="CBEIF_INDENT"></a><a id="cbeif_indent"></a><dl>
<dt><b>CBEIF_INDENT</b></dt>
</dl>
</td>
<td width="60%">
The 
						<b>iIndent</b> member is valid or must be filled in.

</td>
</tr>
<tr>
<td width="40%"><a id="CBEIF_LPARAM"></a><a id="cbeif_lparam"></a><dl>
<dt><b>CBEIF_LPARAM</b></dt>
</dl>
</td>
<td width="60%">
The 
						<b>lParam</b> member is valid or must be filled in.

</td>
</tr>
<tr>
<td width="40%"><a id="CBEIF_OVERLAY"></a><a id="cbeif_overlay"></a><dl>
<dt><b>CBEIF_OVERLAY</b></dt>
</dl>
</td>
<td width="60%">
The 
						<b>iOverlay</b> member is valid or must be filled in.

</td>
</tr>
<tr>
<td width="40%"><a id="CBEIF_SELECTEDIMAGE"></a><a id="cbeif_selectedimage"></a><dl>
<dt><b>CBEIF_SELECTEDIMAGE</b></dt>
</dl>
</td>
<td width="60%">
The 
						<b>iSelectedImage</b> member is valid or must be filled in.

</td>
</tr>
<tr>
<td width="40%"><a id="CBEIF_TEXT"></a><a id="cbeif_text"></a><dl>
<dt><b>CBEIF_TEXT</b></dt>
</dl>
</td>
<td width="60%">
The 
						<b>pszText</b> member is valid or must be filled in.

</td>
</tr>
</table>

### -field iItem

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT_PTR</a></b>

The zero-based index of the item.

### -field pszText

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPTSTR</a></b>

A pointer to a character buffer that contains or receives the item's text. If text information is being retrieved, this member must be set to the address of a character buffer that will receive the text. The size of this buffer must also be indicated in 
					<b>cchTextMax</b>. If this member is set to LPSTR_TEXTCALLBACK, the control will request the information by using the <a href="/windows/desktop/Controls/cben-getdispinfo">CBEN_GETDISPINFO</a> notification codes.

### -field cchTextMax

Type: <b>int</b>

The length of <b>pszText</b>, in <b>TCHAR</b><b>s</b>. If text information is being set, this member is ignored.

### -field iImage

Type: <b>int</b>

The zero-based index of an image within the image list. The specified image will be displayed for the item when it is not selected. If this member is set to I_IMAGECALLBACK, the control will request the information by using <a href="/windows/desktop/Controls/cben-getdispinfo">CBEN_GETDISPINFO</a> notification codes.

### -field iSelectedImage

Type: <b>int</b>

The zero-based index of an image within the image list. The specified image will be displayed for the item when it is selected. If this member is set to I_IMAGECALLBACK, the control will request the information by using <a href="/windows/desktop/Controls/cben-getdispinfo">CBEN_GETDISPINFO</a> notification codes.

### -field iOverlay

Type: <b>int</b>

The one-based index of an overlay image within the image list. If this member is set to I_IMAGECALLBACK, the control will request the information by using <a href="/windows/desktop/Controls/cben-getdispinfo">CBEN_GETDISPINFO</a> notification codes.

### -field iIndent

Type: <b>int</b>

The number of indent spaces to display for the item. Each indentation equals 10 pixels. If this member is set to I_INDENTCALLBACK, the control will request the information by using <a href="/windows/desktop/Controls/cben-getdispinfo">CBEN_GETDISPINFO</a> notification codes.

### -field lParam

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

A value specific to the item.

## -remarks

> [!NOTE]
> The commctrl.h header defines COMBOBOXEXITEM as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
