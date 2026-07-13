---
UID: NS:commctrl.tagTCITEMHEADERW
title: TCITEMHEADERW (commctrl.h)
description: Specifies or receives the attributes of a tab. It is used with the TCM_INSERTITEM, TCM_GETITEM, and TCM_SETITEM messages. This structure supersedes the TC_ITEMHEADER structure. (Unicode)
helpviewer_keywords: ["*LPTCITEMHEADERW","LPTCITEMHEADER","LPTCITEMHEADER structure pointer [Windows Controls]","TCIF_IMAGE","TCIF_RTLREADING","TCIF_TEXT","TCITEMHEADER","TCITEMHEADER structure [Windows Controls]","TCITEMHEADERA","TCITEMHEADERW","_win32_TCITEMHEADER","_win32_TCITEMHEADER_cpp","commctrl/LPTCITEMHEADER","commctrl/TCITEMHEADER","commctrl/TCITEMHEADERA","commctrl/TCITEMHEADERW","controls.TCITEMHEADER","controls._win32_TCITEMHEADER"]
old-location: controls\TCITEMHEADER.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\tab\structures\tcitemheader.htm
ms.date: 12/05/2018
ms.keywords: '*LPTCITEMHEADERW, LPTCITEMHEADER, LPTCITEMHEADER structure pointer [Windows Controls], TCIF_IMAGE, TCIF_RTLREADING, TCIF_TEXT, TCITEMHEADER, TCITEMHEADER structure [Windows Controls], TCITEMHEADERA, TCITEMHEADERW, _win32_TCITEMHEADER, _win32_TCITEMHEADER_cpp, commctrl/LPTCITEMHEADER, commctrl/TCITEMHEADER, commctrl/TCITEMHEADERA, commctrl/TCITEMHEADERW, controls.TCITEMHEADER, controls._win32_TCITEMHEADER'
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: TCITEMHEADERW (Unicode) and TCITEMHEADERA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TCITEMHEADERW, *LPTCITEMHEADERW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagTCITEMHEADERW
 - commctrl/tagTCITEMHEADERW
 - LPTCITEMHEADERW
 - commctrl/LPTCITEMHEADERW
 - TCITEMHEADERW
 - commctrl/TCITEMHEADERW
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
 - TCITEMHEADER
 - TCITEMHEADERA
 - TCITEMHEADERW
---

# TCITEMHEADERW structure


## -description

Specifies or receives the attributes of a tab. It is used with the <a href="/windows/desktop/Controls/tcm-insertitem">TCM_INSERTITEM</a>, <a href="/windows/desktop/Controls/tcm-getitem">TCM_GETITEM</a>, and <a href="/windows/desktop/Controls/tcm-setitem">TCM_SETITEM</a> messages. This structure supersedes the
	<b>TC_ITEMHEADER</b> structure.

## -struct-fields

### -field mask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Value that specifies which members to retrieve or set. This member can be a combination of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TCIF_IMAGE"></a><a id="tcif_image"></a><dl>
<dt><b>TCIF_IMAGE</b></dt>
</dl>
</td>
<td width="60%">
The 
						<b>iImage</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="TCIF_RTLREADING"></a><a id="tcif_rtlreading"></a><dl>
<dt><b>TCIF_RTLREADING</b></dt>
</dl>
</td>
<td width="60%">
The string pointed to by 
						<b>pszText</b> will be displayed in the direction opposite to the text in the parent window.

</td>
</tr>
<tr>
<td width="40%"><a id="TCIF_TEXT"></a><a id="tcif_text"></a><dl>
<dt><b>TCIF_TEXT</b></dt>
</dl>
</td>
<td width="60%">
The 
						<b>pszText</b> member is valid.

</td>
</tr>
</table>

### -field lpReserved1

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Reserved member. Do not use.

### -field lpReserved2

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Reserved member. Do not use.

### -field pszText

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPTSTR</a></b>

Address of a null-terminated string that contains the tab text if item information is being set. If item information is being retrieved, this member specifies the address of the buffer that receives the tab text.

### -field cchTextMax

Type: <b>int</b>

Size of the buffer pointed to by the pszText member. If the structure is not receiving information, this member is ignored.

### -field iImage

Type: <b>int</b>

Index into the tab control's image list, or -1 if there is no image for the tab.

## -remarks

Typically, windows display text left-to-right (LTR). Windows can be 
				<i>mirrored</i> to display languages such as Hebrew or Arabic that read right-to-left (RTL). Ordinarily, 
				<b>pszText</b> will be displayed in the same direction as the text in its parent window. If TCIF_RTLREADING is set, 
				<b>pszText</b> will read in the opposite direction from the text in the parent window.




> [!NOTE]
> The commctrl.h header defines TCITEMHEADER as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
