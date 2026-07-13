---
UID: NS:commctrl.TBBUTTONINFOW
title: TBBUTTONINFOW (commctrl.h)
description: Contains or receives information for a specific button in a toolbar. (Unicode)
helpviewer_keywords: ["*LPTBBUTTONINFOW","LPTBBUTTONINFO","LPTBBUTTONINFO structure pointer [Windows Controls]","TBBUTTONINFO","TBBUTTONINFO structure [Windows Controls]","TBBUTTONINFOA","TBBUTTONINFOW","TBIF_BYINDEX","TBIF_COMMAND","TBIF_IMAGE","TBIF_LPARAM","TBIF_SIZE","TBIF_STATE","TBIF_STYLE","TBIF_TEXT","_win32_TBBUTTONINFO","_win32_TBBUTTONINFO_cpp","commctrl/LPTBBUTTONINFO","commctrl/TBBUTTONINFO","commctrl/TBBUTTONINFOA","commctrl/TBBUTTONINFOW","controls.TBBUTTONINFO","controls._win32_TBBUTTONINFO"]
old-location: controls\TBBUTTONINFO.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\toolbar\structures\tbbuttoninfo.htm
ms.date: 12/05/2018
ms.keywords: '*LPTBBUTTONINFOW, LPTBBUTTONINFO, LPTBBUTTONINFO structure pointer [Windows Controls], TBBUTTONINFO, TBBUTTONINFO structure [Windows Controls], TBBUTTONINFOA, TBBUTTONINFOW, TBIF_BYINDEX, TBIF_COMMAND, TBIF_IMAGE, TBIF_LPARAM, TBIF_SIZE, TBIF_STATE, TBIF_STYLE, TBIF_TEXT, _win32_TBBUTTONINFO, _win32_TBBUTTONINFO_cpp, commctrl/LPTBBUTTONINFO, commctrl/TBBUTTONINFO, commctrl/TBBUTTONINFOA, commctrl/TBBUTTONINFOW, controls.TBBUTTONINFO, controls._win32_TBBUTTONINFO'
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: TBBUTTONINFOW (Unicode) and TBBUTTONINFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TBBUTTONINFOW, *LPTBBUTTONINFOW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPTBBUTTONINFOW
 - commctrl/LPTBBUTTONINFOW
 - TBBUTTONINFOW
 - commctrl/TBBUTTONINFOW
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
 - TBBUTTONINFO
 - TBBUTTONINFOA
 - TBBUTTONINFOW
---

# TBBUTTONINFOW structure


## -description

Contains or receives information for a specific button in a toolbar.

## -struct-fields

### -field cbSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Size of the structure, in bytes. This member must be filled in prior to sending the associated message.

### -field dwMask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Set of flags that indicate which members contain valid information. This member must be filled in prior to sending the associated message. This can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TBIF_BYINDEX"></a><a id="tbif_byindex"></a><dl>
<dt><b>TBIF_BYINDEX</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 5.80.</a> The <i>wParam</i> sent with a <a href="/windows/desktop/Controls/tb-getbuttoninfo">TB_GETBUTTONINFO</a> or <a href="/windows/desktop/Controls/tb-setbuttoninfo">TB_SETBUTTONINFO</a> message is an index, not an identifier.

</td>
</tr>
<tr>
<td width="40%"><a id="TBIF_COMMAND"></a><a id="tbif_command"></a><dl>
<dt><b>TBIF_COMMAND</b></dt>
</dl>
</td>
<td width="60%">
The <b>idCommand</b> member contains valid information or is being requested.

</td>
</tr>
<tr>
<td width="40%"><a id="TBIF_IMAGE"></a><a id="tbif_image"></a><dl>
<dt><b>TBIF_IMAGE</b></dt>
</dl>
</td>
<td width="60%">
The <b>iImage</b> member contains valid information or is being requested.

</td>
</tr>
<tr>
<td width="40%"><a id="TBIF_LPARAM"></a><a id="tbif_lparam"></a><dl>
<dt><b>TBIF_LPARAM</b></dt>
</dl>
</td>
<td width="60%">
The <b>lParam</b> member contains valid information or is being requested.

</td>
</tr>
<tr>
<td width="40%"><a id="TBIF_SIZE"></a><a id="tbif_size"></a><dl>
<dt><b>TBIF_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The <b>cx</b> member contains valid information or is being requested.

</td>
</tr>
<tr>
<td width="40%"><a id="TBIF_STATE"></a><a id="tbif_state"></a><dl>
<dt><b>TBIF_STATE</b></dt>
</dl>
</td>
<td width="60%">
The <b>fsState</b> member contains valid information or is being requested.

</td>
</tr>
<tr>
<td width="40%"><a id="TBIF_STYLE"></a><a id="tbif_style"></a><dl>
<dt><b>TBIF_STYLE</b></dt>
</dl>
</td>
<td width="60%">
The <b>fsStyle</b> member contains valid information or is being requested.

</td>
</tr>
<tr>
<td width="40%"><a id="TBIF_TEXT"></a><a id="tbif_text"></a><dl>
<dt><b>TBIF_TEXT</b></dt>
</dl>
</td>
<td width="60%">
The <b>pszText</b> member contains valid information or is being requested.

</td>
</tr>
</table>

### -field idCommand

Type: <b>int</b>

Command identifier of the button.

### -field iImage

Type: <b>int</b>

Image index of the button. Set this member to I_IMAGECALLBACK, and the toolbar will send the <a href="/windows/desktop/Controls/tbn-getdispinfo">TBN_GETDISPINFO</a> notification code to retrieve the image index when it is needed. 
                    


<a href="/windows/desktop/Controls/common-control-versions">Version 5.81</a>. Set this member to I_IMAGENONE to indicate that the button does not have an image. The button layout will not include any space for a bitmap, only text.

### -field fsState

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

State flags of the button. This can be one or more of the values listed in  <a href="/windows/desktop/Controls/toolbar-button-states">Toolbar Button States</a>.

### -field fsStyle

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

Style flags of the button. This can be one or more of the values listed in <a href="/windows/desktop/Controls/toolbar-control-and-button-styles">Toolbar Control and Button Styles</a>.

### -field cx

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WORD</a></b>

Width of the button, in pixels.

### -field lParam

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD_PTR</a></b>

Application-defined value associated with the button.

### -field pszText

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPTSTR</a></b>

Address of a character buffer that contains or receives the button text.

### -field cchText

Type: <b>int</b>

Size of the buffer at <b>pszText</b>. If the button information is being set, this member is ignored.

## -remarks

> [!NOTE]
> The commctrl.h header defines TBBUTTONINFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

