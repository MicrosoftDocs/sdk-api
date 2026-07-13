---
UID: NS:commctrl.tagNMHDDISPINFOW
title: NMHDDISPINFOW (commctrl.h)
description: Contains information used in handling HDN_GETDISPINFO notification codes. (Unicode)
helpviewer_keywords: ["*LPNMHDDISPINFOW","HDI_DI_SETITEM","HDI_IMAGE","HDI_LPARAM","HDI_TEXT","LPNMHDDISPINFO","LPNMHDDISPINFO structure pointer [Windows Controls]","NMHDDISPINFO","NMHDDISPINFO structure [Windows Controls]","NMHDDISPINFOA","NMHDDISPINFOW","_win32_NMHDDISPINFO","_win32_NMHDDISPINFO_cpp","commctrl/LPNMHDDISPINFO","commctrl/NMHDDISPINFO","commctrl/NMHDDISPINFOA","commctrl/NMHDDISPINFOW","controls.NMHDDISPINFO","controls._win32_NMHDDISPINFO"]
old-location: controls\NMHDDISPINFO.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\header\structures\nmhddispinfo.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMHDDISPINFOW, HDI_DI_SETITEM, HDI_IMAGE, HDI_LPARAM, HDI_TEXT, LPNMHDDISPINFO, LPNMHDDISPINFO structure pointer [Windows Controls], NMHDDISPINFO, NMHDDISPINFO structure [Windows Controls], NMHDDISPINFOA, NMHDDISPINFOW, _win32_NMHDDISPINFO, _win32_NMHDDISPINFO_cpp, commctrl/LPNMHDDISPINFO, commctrl/NMHDDISPINFO, commctrl/NMHDDISPINFOA, commctrl/NMHDDISPINFOW, controls.NMHDDISPINFO, controls._win32_NMHDDISPINFO'
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: NMHDDISPINFOW (Unicode) and NMHDDISPINFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NMHDDISPINFOW, *LPNMHDDISPINFOW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNMHDDISPINFOW
 - commctrl/tagNMHDDISPINFOW
 - LPNMHDDISPINFOW
 - commctrl/LPNMHDDISPINFOW
 - NMHDDISPINFOW
 - commctrl/NMHDDISPINFOW
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
 - NMHDDISPINFO
 - NMHDDISPINFOA
 - NMHDDISPINFOW
---

# NMHDDISPINFOW structure


## -description

Contains information used in handling <a href="/windows/desktop/Controls/hdn-getdispinfo">HDN_GETDISPINFO</a> notification codes.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>


<a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure containing information about this notification code.

### -field iItem

Type: <b>int</b>

The zero-based index of the item in the header control.

### -field mask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A set of bit flags specifying which members of the structure must be filled in by the owner of the header control. This value can be a combination of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HDI_TEXT"></a><a id="hdi_text"></a><dl>
<dt><b>HDI_TEXT</b></dt>
</dl>
</td>
<td width="60%">
The 
						<b>pszText</b> field must be filled in.

</td>
</tr>
<tr>
<td width="40%"><a id="HDI_IMAGE"></a><a id="hdi_image"></a><dl>
<dt><b>HDI_IMAGE</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 4.70</a>. The 
						<b>iImage</b> field must be filled in.

</td>
</tr>
<tr>
<td width="40%"><a id="HDI_LPARAM"></a><a id="hdi_lparam"></a><dl>
<dt><b>HDI_LPARAM</b></dt>
</dl>
</td>
<td width="60%">
The 
						<b>lParam</b> field must be filled in.

</td>
</tr>
<tr>
<td width="40%"><a id="HDI_DI_SETITEM"></a><a id="hdi_di_setitem"></a><dl>
<dt><b>HDI_DI_SETITEM</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 4.70</a>. A return value. Indicates that the header control should store the item information and not ask for it again.

</td>
</tr>
</table>

### -field pszText

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPTSTR</a></b>

A pointer to a null-terminated string containing the text that will be displayed for the header item.

### -field cchTextMax

Type: <b>int</b>

The size of the buffer that 
					<b>pszText</b> points to.

### -field iImage

Type: <b>int</b>

The zero-based index of an image within the image list. The specified image will be displayed with the header item, but it does not take the place of the item's bitmap. If 
					<b>iImage</b> is set to I_IMAGECALLBACK, the control requests image information for this item by using an <a href="/windows/desktop/Controls/hdn-getdispinfo">HDN_GETDISPINFO</a> notification code.

### -field lParam

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

An application-defined value to associate with the item.

## -remarks

> [!NOTE]
> The commctrl.h header defines NMHDDISPINFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
