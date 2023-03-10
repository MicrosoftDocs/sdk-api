---
UID: NS:winuser.tagCURSORINFO
title: CURSORINFO (winuser.h)
description: Contains global cursor information.
helpviewer_keywords: ["*LPCURSORINFO","*PCURSORINFO","CURSORINFO","CURSORINFO structure [Menus and Other Resources]","CURSOR_SHOWING","CURSOR_SUPPRESSED","LPCURSORINFO","LPCURSORINFO structure pointer [Menus and Other Resources]","PCURSORINFO","PCURSORINFO structure pointer [Menus and Other Resources]","_win32_CURSORINFO_str","_win32_cursorinfo_str_cpp","menurc.cursorinfo","winui._win32_cursorinfo_str","winuser/CURSORINFO","winuser/LPCURSORINFO","winuser/PCURSORINFO"]
old-location: menurc\cursorinfo.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\cursors\cursorreference\cursorstructures\cursorinfo.htm
ms.date: 12/05/2018
ms.keywords: '*LPCURSORINFO, *PCURSORINFO, CURSORINFO, CURSORINFO structure [Menus and Other Resources], CURSOR_SHOWING, CURSOR_SUPPRESSED, LPCURSORINFO, LPCURSORINFO structure pointer [Menus and Other Resources], PCURSORINFO, PCURSORINFO structure pointer [Menus and Other Resources], _win32_CURSORINFO_str, _win32_cursorinfo_str_cpp, menurc.cursorinfo, winui._win32_cursorinfo_str, winuser/CURSORINFO, winuser/LPCURSORINFO, winuser/PCURSORINFO'
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
req.typenames: CURSORINFO, *PCURSORINFO, *LPCURSORINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCURSORINFO
 - winuser/tagCURSORINFO
 - PCURSORINFO
 - winuser/PCURSORINFO
 - CURSORINFO
 - winuser/CURSORINFO
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
 - CURSORINFO
---

# CURSORINFO structure


## -description

Contains global cursor information.

## -struct-fields

### -field cbSize

Type: <b>DWORD</b>

The size of the structure, in bytes. The caller must set this to <code>sizeof(CURSORINFO)</code>.

### -field flags

Type: <b>DWORD</b>

The cursor state. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The cursor is hidden.

</td>
</tr>
<tr>
<td width="40%"><a id="CURSOR_SHOWING"></a><a id="cursor_showing"></a><dl>
<dt><b>CURSOR_SHOWING</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The cursor is showing.

</td>
</tr>
<tr>
<td width="40%"><a id="CURSOR_SUPPRESSED"></a><a id="cursor_suppressed"></a><dl>
<dt><b>CURSOR_SUPPRESSED</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
<b>Windows 8</b>: The cursor is suppressed. This flag indicates that the system is not drawing the cursor because the user is providing input through touch or pen instead of the mouse.

</td>
</tr>
</table>

### -field hCursor

Type: <b>HCURSOR</b>

A handle to the cursor.

### -field ptScreenPos

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a></b>

A   structure that receives the screen coordinates of the cursor.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/menurc/cursors">Cursors</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getcursorinfo">GetCursorInfo</a>



<a href="/windows/win32/api/windef/ns-windef-point">POINT</a>



<b>Reference</b>