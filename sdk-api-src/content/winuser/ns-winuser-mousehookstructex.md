---
UID: NS:winuser.tagMOUSEHOOKSTRUCTEX
title: MOUSEHOOKSTRUCTEX (winuser.h)
description: Contains information about a mouse event passed to a WH_MOUSE hook procedure, MouseProc. This is an extension of the MOUSEHOOKSTRUCT structure that includes information about wheel movement or the use of the X button.
helpviewer_keywords: ["*LPMOUSEHOOKSTRUCTEX","*PMOUSEHOOKSTRUCTEX","LPMOUSEHOOKSTRUCTEX","LPMOUSEHOOKSTRUCTEX structure pointer [Windows and Messages]","MOUSEHOOKSTRUCTEX","MOUSEHOOKSTRUCTEX structure [Windows and Messages]","PMOUSEHOOKSTRUCTEX","PMOUSEHOOKSTRUCTEX structure pointer [Windows and Messages]","XBUTTON1","XBUTTON2","_win32_MOUSEHOOKSTRUCTEX_str","_win32_mousehookstructex_str_cpp","winmsg.mousehookstructex","winui._win32_mousehookstructex_str","winuser/LPMOUSEHOOKSTRUCTEX","winuser/MOUSEHOOKSTRUCTEX","winuser/PMOUSEHOOKSTRUCTEX"]
old-location: winmsg\mousehookstructex.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\hooks\hookreference\hookstructures\mousehookstructex.htm
ms.date: 12/05/2018
ms.keywords: '*LPMOUSEHOOKSTRUCTEX, *PMOUSEHOOKSTRUCTEX, LPMOUSEHOOKSTRUCTEX, LPMOUSEHOOKSTRUCTEX structure pointer [Windows and Messages], MOUSEHOOKSTRUCTEX, MOUSEHOOKSTRUCTEX structure [Windows and Messages], PMOUSEHOOKSTRUCTEX, PMOUSEHOOKSTRUCTEX structure pointer [Windows and Messages], XBUTTON1, XBUTTON2, _win32_MOUSEHOOKSTRUCTEX_str, _win32_mousehookstructex_str_cpp, winmsg.mousehookstructex, winui._win32_mousehookstructex_str, winuser/LPMOUSEHOOKSTRUCTEX, winuser/MOUSEHOOKSTRUCTEX, winuser/PMOUSEHOOKSTRUCTEX'
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: MOUSEHOOKSTRUCTEX, *LPMOUSEHOOKSTRUCTEX, *PMOUSEHOOKSTRUCTEX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMOUSEHOOKSTRUCTEX
 - winuser/tagMOUSEHOOKSTRUCTEX
 - LPMOUSEHOOKSTRUCTEX
 - winuser/LPMOUSEHOOKSTRUCTEX
 - MOUSEHOOKSTRUCTEX
 - winuser/MOUSEHOOKSTRUCTEX
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - MOUSEHOOKSTRUCTEX
---

# MOUSEHOOKSTRUCTEX structure


## -description

Contains information about a mouse event passed to a <b>WH_MOUSE</b> hook procedure, <a href="/windows/win32/winmsg/mouseproc">MouseProc</a>. 

This is an extension of the <a href="/windows/desktop/api/winuser/ns-winuser-mousehookstruct">MOUSEHOOKSTRUCT</a> structure that includes information about wheel movement or the use of the X button.

## -struct-fields

### -field mouseData

Type: <b>DWORD</b>

If the message is <a href="/windows/desktop/inputdev/wm-mousewheel">WM_MOUSEWHEEL</a>, the HIWORD of this member is the wheel delta. The LOWORD is undefined and reserved. A positive value indicates that the wheel was rotated forward, away from the user; a negative value indicates that the wheel was rotated backward, toward the user. One wheel click is defined as WHEEL_DELTA, which is 120. 

If the message is <a href="/windows/desktop/inputdev/wm-xbuttondown">WM_XBUTTONDOWN</a>, <a href="/windows/desktop/inputdev/wm-xbuttonup">WM_XBUTTONUP</a>, <a href="/windows/desktop/inputdev/wm-xbuttondblclk">WM_XBUTTONDBLCLK</a>, <a href="/windows/desktop/inputdev/wm-ncxbuttondown">WM_NCXBUTTONDOWN</a>, <a href="/windows/desktop/inputdev/wm-ncxbuttonup">WM_NCXBUTTONUP</a>, or <a href="/windows/desktop/inputdev/wm-ncxbuttondblclk">WM_NCXBUTTONDBLCLK</a>, the HIWORD of 
						<b>mouseData</b> specifies which X button was pressed or released, and the LOWORD is undefined and reserved. This member can be one or more of the following values. Otherwise, 
						<b>mouseData</b> is not used. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="XBUTTON1"></a><a id="xbutton1"></a><dl>
<dt><b>XBUTTON1</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
The first X button was pressed or released.

</td>
</tr>
<tr>
<td width="40%"><a id="XBUTTON2"></a><a id="xbutton2"></a><dl>
<dt><b>XBUTTON2</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
The second X button was pressed or released.

</td>
</tr>
</table>

### -field tagMOUSEHOOKSTRUCT

Type: <b><a href="/windows/desktop/api/winuser/ns-winuser-mousehookstruct">MOUSEHOOKSTRUCT</a></b>

The members of a <a href="/windows/desktop/api/winuser/ns-winuser-mousehookstruct">MOUSEHOOKSTRUCT</a> structure make up the first part of this structure.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/winmsg/hooks">Hooks</a>



<a href="/windows/desktop/api/winuser/ns-winuser-mousehookstruct">MOUSEHOOKSTRUCT</a>



<a href="/windows/win32/winmsg/mouseproc">MouseProc</a>



<b>Reference</b>



<a href="/windows/desktop/inputdev/wm-mousewheel">WM_MOUSEWHEEL</a>



<a href="/windows/desktop/inputdev/wm-ncxbuttondblclk">WM_NCXBUTTONDBLCLK</a>



<a href="/windows/desktop/inputdev/wm-ncxbuttondown">WM_NCXBUTTONDOWN</a>



<a href="/windows/desktop/inputdev/wm-ncxbuttonup">WM_NCXBUTTONUP</a>



<a href="/windows/desktop/inputdev/wm-xbuttondblclk">WM_XBUTTONDBLCLK</a>



<a href="/windows/desktop/inputdev/wm-xbuttondown">WM_XBUTTONDOWN</a>



<a href="/windows/desktop/inputdev/wm-xbuttonup">WM_XBUTTONUP</a>