---
UID: NS:winuser.tagGUITHREADINFO
title: GUITHREADINFO (winuser.h)
description: Contains information about a GUI thread.
helpviewer_keywords: ["*LPGUITHREADINFO","*PGUITHREADINFO","GUITHREADINFO","GUITHREADINFO structure [Windows and Messages]","GUI_CARETBLINKING","GUI_INMENUMODE","GUI_INMOVESIZE","GUI_POPUPMENUMODE","GUI_SYSTEMMENUMODE","PGUITHREADINFO","PGUITHREADINFO structure pointer [Windows and Messages]","_win32_GUITHREADINFO_str","_win32_guithreadinfo_str_cpp","winmsg.guithreadinfo","winui._win32_guithreadinfo_str","winuser/GUITHREADINFO","winuser/PGUITHREADINFO"]
old-location: winmsg\guithreadinfo.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowstructures\guithreadinfo.htm
ms.date: 12/05/2018
ms.keywords: '*LPGUITHREADINFO, *PGUITHREADINFO, GUITHREADINFO, GUITHREADINFO structure [Windows and Messages], GUI_CARETBLINKING, GUI_INMENUMODE, GUI_INMOVESIZE, GUI_POPUPMENUMODE, GUI_SYSTEMMENUMODE, PGUITHREADINFO, PGUITHREADINFO structure pointer [Windows and Messages], _win32_GUITHREADINFO_str, _win32_guithreadinfo_str_cpp, winmsg.guithreadinfo, winui._win32_guithreadinfo_str, winuser/GUITHREADINFO, winuser/PGUITHREADINFO'
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
req.typenames: GUITHREADINFO, *PGUITHREADINFO, *LPGUITHREADINFO
req.redist: Service Pack 3
ms.custom: 19H1
f1_keywords:
 - tagGUITHREADINFO
 - winuser/tagGUITHREADINFO
 - PGUITHREADINFO
 - winuser/PGUITHREADINFO
 - GUITHREADINFO
 - winuser/GUITHREADINFO
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
 - GUITHREADINFO
---

# GUITHREADINFO structure


## -description

Contains information about a GUI thread.

## -struct-fields

### -field cbSize

Type: <b>DWORD</b>

The size of this structure, in bytes. The caller must set this member to <code>sizeof(GUITHREADINFO)</code>.

### -field flags

Type: <b>DWORD</b>

The thread state. This member can be one or more of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GUI_CARETBLINKING"></a><a id="gui_caretblinking"></a><dl>
<dt><b>GUI_CARETBLINKING</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The caret's blink state. This bit is set if the caret is visible. 

</td>
</tr>
<tr>
<td width="40%"><a id="GUI_INMENUMODE"></a><a id="gui_inmenumode"></a><dl>
<dt><b>GUI_INMENUMODE</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The thread's menu state. This bit is set if the thread is in menu mode. 

</td>
</tr>
<tr>
<td width="40%"><a id="GUI_INMOVESIZE"></a><a id="gui_inmovesize"></a><dl>
<dt><b>GUI_INMOVESIZE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The thread's move state. This bit is set if the thread is in a move or size loop. 

</td>
</tr>
<tr>
<td width="40%"><a id="GUI_POPUPMENUMODE"></a><a id="gui_popupmenumode"></a><dl>
<dt><b>GUI_POPUPMENUMODE</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
The thread's pop-up menu state. This bit is set if the thread has an active pop-up menu.

</td>
</tr>
<tr>
<td width="40%"><a id="GUI_SYSTEMMENUMODE"></a><a id="gui_systemmenumode"></a><dl>
<dt><b>GUI_SYSTEMMENUMODE</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The thread's system menu state. This bit is set if the thread is in a system menu mode.

</td>
</tr>
</table>

### -field hwndActive

Type: <b>HWND</b>

A handle to the active window within the thread.

### -field hwndFocus

Type: <b>HWND</b>

A handle to the window that has the keyboard focus.

### -field hwndCapture

Type: <b>HWND</b>

A handle to the window that has captured the mouse.

### -field hwndMenuOwner

Type: <b>HWND</b>

A handle to the window that owns any active menus.

### -field hwndMoveSize

Type: <b>HWND</b>

A handle to the window in a move or size loop.

### -field hwndCaret

Type: <b>HWND</b>

A handle to the window that is displaying the caret.

### -field rcCaret

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>

The caret's bounding rectangle, in client coordinates, relative to the window specified by the <b>hwndCaret</b> member.

## -remarks

This structure is used with the <a href="/windows/desktop/api/winuser/nf-winuser-getguithreadinfo">GetGUIThreadInfo</a> function to retrieve information about the active window or a specified GUI thread.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getguithreadinfo">GetGUIThreadInfo</a>



<b>Reference</b>



<a href="/windows/desktop/winmsg/windows">Windows</a>