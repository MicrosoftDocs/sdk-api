---
UID: NS:commctrl.tagNMTTDISPINFOW
title: NMTTDISPINFOW (commctrl.h)
description: Contains information used in handling the TTN_GETDISPINFO notification code. This structure supersedes the TOOLTIPTEXT structure. (Unicode)
helpviewer_keywords: ["*LPNMTTDISPINFOW","LPNMTTDISPINFO","LPNMTTDISPINFO structure pointer [Windows Controls]","NMTTDISPINFO","NMTTDISPINFO structure [Windows Controls]","NMTTDISPINFOA","NMTTDISPINFOW","TTF_DI_SETITEM","TTF_IDISHWND","TTF_RTLREADING","_win32_NMTTDISPINFO","_win32_NMTTDISPINFO_cpp","commctrl/LPNMTTDISPINFO","commctrl/NMTTDISPINFO","commctrl/NMTTDISPINFOA","commctrl/NMTTDISPINFOW","controls.NMTTDISPINFO","controls._win32_NMTTDISPINFO"]
old-location: controls\NMTTDISPINFO.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\tooltip\structures\tooltiptext.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMTTDISPINFOW, LPNMTTDISPINFO, LPNMTTDISPINFO structure pointer [Windows Controls], NMTTDISPINFO, NMTTDISPINFO structure [Windows Controls], NMTTDISPINFOA, NMTTDISPINFOW, TTF_DI_SETITEM, TTF_IDISHWND, TTF_RTLREADING, _win32_NMTTDISPINFO, _win32_NMTTDISPINFO_cpp, commctrl/LPNMTTDISPINFO, commctrl/NMTTDISPINFO, commctrl/NMTTDISPINFOA, commctrl/NMTTDISPINFOW, controls.NMTTDISPINFO, controls._win32_NMTTDISPINFO'
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: NMTTDISPINFOW (Unicode) and NMTTDISPINFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NMTTDISPINFOW, *LPNMTTDISPINFOW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNMTTDISPINFOW
 - commctrl/tagNMTTDISPINFOW
 - LPNMTTDISPINFOW
 - commctrl/LPNMTTDISPINFOW
 - NMTTDISPINFOW
 - commctrl/NMTTDISPINFOW
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
 - NMTTDISPINFO
 - NMTTDISPINFOA
 - NMTTDISPINFOW
---

# NMTTDISPINFOW structure


## -description

Contains information used in handling the <a href="/windows/desktop/Controls/ttn-getdispinfo">TTN_GETDISPINFO</a> notification code. This structure supersedes the 
			<b>TOOLTIPTEXT</b> structure.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>


<a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains additional information about the notification.

### -field lpszText

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPTSTR</a></b>

Pointer to a null-terminated string that will be displayed as the tooltip text. If <b>hinst</b> specifies an instance handle, this member must be the identifier of a string resource.

### -field szText

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">TCHAR</a></b>

Buffer that receives the tooltip text. An application can copy the text to this buffer instead of specifying a string address or string resource. For tooltip text that exceeds 80 <b>TCHAR</b><b>s</b>, see comments in the remarks section of this document.

### -field hinst

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HINSTANCE</a></b>

Handle to the instance that contains a string resource to be used as the tooltip text. If <b>lpszText</b> is the address of the tooltip text string, this member must be <b>NULL</b>.

### -field uFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Flags that indicates how to interpret the <b>idFrom</b> member of the included <a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TTF_IDISHWND"></a><a id="ttf_idishwnd"></a><dl>
<dt><b>TTF_IDISHWND</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, <b>idFrom</b> is the tool's handle. Otherwise, it is the tool's identifier. 

</td>
</tr>
<tr>
<td width="40%"><a id="TTF_RTLREADING"></a><a id="ttf_rtlreading"></a><dl>
<dt><b>TTF_RTLREADING</b></dt>
</dl>
</td>
<td width="60%">
Windows can be 
						<i>mirrored</i> to display languages such as Hebrew or Arabic that read right-to-left (RTL). Normally, tooltip text is read in same direction as the text in its parent window. To have a tooltip read in the opposite direction from its parent window, add the TTF_RTLREADING flag to the 
						<b>uFlags</b> member when processing the notification. 

</td>
</tr>
<tr>
<td width="40%"><a id="TTF_DI_SETITEM"></a><a id="ttf_di_setitem"></a><dl>
<dt><b>TTF_DI_SETITEM</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 4.70</a>. If you add this flag to <b>uFlags</b> while processing the notification, the tooltip control will retain the supplied information and not request it again. 

</td>
</tr>
</table>

### -field lParam

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>


<a href="/windows/desktop/Controls/common-control-versions">Version 4.70</a>. Application-defined data associated with the tool.

## -remarks

You need to point the <b>lpszText</b> array to your own private buffer when the text used in the tooltip exceeds 80 <b>TCHAR</b>s in length. The system automatically strips the ampersand (&amp;) accelerator <b>TCHAR</b><b>s</b> from all strings passed to a tooltip control, unless the control has the <a href="/windows/desktop/Controls/tooltip-styles">TTS_NOPREFIX</a> style.




> [!NOTE]
> The commctrl.h header defines NMTTDISPINFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
