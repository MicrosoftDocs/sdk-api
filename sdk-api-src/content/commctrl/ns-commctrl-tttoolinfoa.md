---
UID: NS:commctrl.tagTOOLINFOA
title: TTTOOLINFOA (commctrl.h)
description: The TOOLINFO structure contains information about a tool in a tooltip control. (ANSI)
helpviewer_keywords: ["*LPTTTOOLINFOA","*PTOOLINFOA","LPTOOLINFO","LPTOOLINFO structure pointer [Windows Controls]","PTOOLINFO","PTOOLINFO structure pointer [Windows Controls]","TOOLINFO","TOOLINFO structure [Windows Controls]","TOOLINFOA","TOOLINFOW","TTF_ABSOLUTE","TTF_CENTERTIP","TTF_IDISHWND","TTF_PARSELINKS","TTF_RTLREADING","TTF_SUBCLASS","TTF_TRACK","TTF_TRANSPARENT","TTTOOLINFO","TTTOOLINFOA","TTTOOLINFOW","_win32_TOOLINFO","_win32_TOOLINFO_cpp","commctrl/LPTOOLINFO","commctrl/PTOOLINFO","commctrl/TOOLINFO","commctrl/TOOLINFOA","commctrl/TOOLINFOW","controls.TOOLINFO","controls._win32_TOOLINFO"]
old-location: controls\TOOLINFO.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\tooltip\structures\toolinfo.htm
ms.date: 12/05/2018
ms.keywords: '*LPTTTOOLINFOA, *PTOOLINFOA, LPTOOLINFO, LPTOOLINFO structure pointer [Windows Controls], PTOOLINFO, PTOOLINFO structure pointer [Windows Controls], TOOLINFO, TOOLINFO structure [Windows Controls], TOOLINFOA, TOOLINFOW, TTF_ABSOLUTE, TTF_CENTERTIP, TTF_IDISHWND, TTF_PARSELINKS, TTF_RTLREADING, TTF_SUBCLASS, TTF_TRACK, TTF_TRANSPARENT, TTTOOLINFO, TTTOOLINFOA, TTTOOLINFOW, _win32_TOOLINFO, _win32_TOOLINFO_cpp, commctrl/LPTOOLINFO, commctrl/PTOOLINFO, commctrl/TOOLINFO, commctrl/TOOLINFOA, commctrl/TOOLINFOW, controls.TOOLINFO, controls._win32_TOOLINFO'
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: TOOLINFOW (Unicode) and TOOLINFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TTTOOLINFOA, *PTOOLINFOA, *LPTTTOOLINFOA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagTOOLINFOA
 - commctrl/tagTOOLINFOA
 - PTOOLINFOA
 - commctrl/PTOOLINFOA
 - TTTOOLINFOA
 - commctrl/TTTOOLINFOA
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
 - TOOLINFO
 - TOOLINFOA
 - TOOLINFOW
 - tttoolinfoa
---

# TTTOOLINFOA structure


## -description

The <b>TOOLINFO</b> structure contains information about a tool in a tooltip control.

## -struct-fields

### -field cbSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Size of this structure, in bytes. This member must be specified.

### -field uFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Flags that control the tooltip display. This member can be a combination of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TTF_ABSOLUTE"></a><a id="ttf_absolute"></a><dl>
<dt><b>TTF_ABSOLUTE</b></dt>
</dl>
</td>
<td width="60%">
Positions the tooltip window at the same coordinates provided by <a href="/windows/desktop/Controls/ttm-trackposition">TTM_TRACKPOSITION</a>. This flag must be used with the TTF_TRACK flag. 

</td>
</tr>
<tr>
<td width="40%"><a id="TTF_CENTERTIP"></a><a id="ttf_centertip"></a><dl>
<dt><b>TTF_CENTERTIP</b></dt>
</dl>
</td>
<td width="60%">
Centers the tooltip window below the tool specified by the <b>uId</b> member. 

</td>
</tr>
<tr>
<td width="40%"><a id="TTF_IDISHWND"></a><a id="ttf_idishwnd"></a><dl>
<dt><b>TTF_IDISHWND</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the <b>uId</b> member is the window handle to the tool. If this flag is not set, <b>uId</b> is the tool's identifier. 

</td>
</tr>
<tr>
<td width="40%"><a id="TTF_PARSELINKS"></a><a id="ttf_parselinks"></a><dl>
<dt><b>TTF_PARSELINKS</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 6.0 and later</a>. Indicates that links in the tooltip text should be parsed.
                        
                        

Note that Comctl32.dll version 6 is not redistributable but it is included in Windows or later. To use Comctl32.dll version 6, specify it in a manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="TTF_RTLREADING"></a><a id="ttf_rtlreading"></a><dl>
<dt><b>TTF_RTLREADING</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the tooltip text will be displayed in the opposite direction to the text in the parent window. 

</td>
</tr>
<tr>
<td width="40%"><a id="TTF_SUBCLASS"></a><a id="ttf_subclass"></a><dl>
<dt><b>TTF_SUBCLASS</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the tooltip control should subclass the tool's window to intercept messages, such as <a href="/windows/desktop/inputdev/wm-mousemove">WM_MOUSEMOVE</a>. If this flag is not set, you must use the <a href="/windows/desktop/Controls/ttm-relayevent">TTM_RELAYEVENT</a> message to forward messages to the tooltip control. For a list of messages that a tooltip control processes, see TTM_RELAYEVENT. 

</td>
</tr>
<tr>
<td width="40%"><a id="TTF_TRACK"></a><a id="ttf_track"></a><dl>
<dt><b>TTF_TRACK</b></dt>
</dl>
</td>
<td width="60%">
Positions the tooltip window next to the tool to which it corresponds and moves the window according to coordinates supplied by the <a href="/windows/desktop/Controls/ttm-trackposition">TTM_TRACKPOSITION</a> messages. You must activate this type of tool using the <a href="/windows/desktop/Controls/ttm-trackactivate">TTM_TRACKACTIVATE</a> message. 

</td>
</tr>
<tr>
<td width="40%"><a id="TTF_TRANSPARENT"></a><a id="ttf_transparent"></a><dl>
<dt><b>TTF_TRANSPARENT</b></dt>
</dl>
</td>
<td width="60%">
Causes the tooltip control to forward mouse event messages to the parent window. This is limited to mouse events that occur within the bounds of the tooltip window. 

</td>
</tr>
</table>

### -field hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the window that contains the tool. If <b>lpszText</b> includes the LPSTR_TEXTCALLBACK value, this member identifies the window that receives the <a href="/windows/desktop/Controls/ttn-getdispinfo">TTN_GETDISPINFO</a> notification codes.

### -field uId

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT_PTR</a></b>

Application-defined identifier of the tool. If <b>uFlags</b> includes the TTF_IDISHWND flag, <b>uId</b> must specify the window handle to the tool.

### -field rect

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>

The bounding rectangle coordinates of the tool. The coordinates are relative to the upper-left corner of the client area of the window identified by <b>hwnd</b>. If <b>uFlags</b> includes the TTF_IDISHWND flag, this member is ignored.

### -field hinst

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HINSTANCE</a></b>

Handle to the instance that contains the string resource for the tool. If <b>lpszText</b> specifies the identifier of a string resource, this member is used.

### -field lpszText

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPTSTR</a></b>

Pointer to the buffer that contains the text for the tool, or identifier of the string resource that contains the text. This member is sometimes used to return values. If you need to examine the returned value,  must point to a valid buffer of sufficient size. Otherwise, it can be set to <b>NULL</b>. If <b>lpszText</b> is set to LPSTR_TEXTCALLBACK, the control sends
the <a href="/windows/desktop/Controls/ttn-getdispinfo">TTN_GETDISPINFO</a> notification code to the owner window to retrieve the text.

### -field lParam

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

<b>Version 4.70 and later</b>. A 32-bit application-defined value that is associated with the tool.

### -field lpReserved

Type: <b>void*</b>

Reserved. Must be set to <b>NULL</b>.

## -remarks

Normal windows display text left-to-right (LTR). Windows can be <i>mirrored</i> to display languages such as Hebrew or Arabic that read right-to-left (RTL). Normally, tooltip text is displayed in the same direction as the text in its parent window. If TTF_RTLREADING is set, tooltip text will read in the opposite direction from the text in the parent window.




> [!NOTE]
> The commctrl.h header defines TTTOOLINFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
