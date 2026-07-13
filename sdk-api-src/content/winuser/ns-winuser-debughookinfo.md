---
UID: NS:winuser.tagDEBUGHOOKINFO
title: DEBUGHOOKINFO (winuser.h)
description: Contains debugging information passed to a WH_DEBUG hook procedure, DebugProc.
helpviewer_keywords: ["*LPDEBUGHOOKINFO","*NPDEBUGHOOKINFO","*PDEBUGHOOKINFO","DEBUGHOOKINFO","DEBUGHOOKINFO structure [Windows and Messages]","LPDEBUGHOOKINFO","LPDEBUGHOOKINFO structure pointer [Windows and Messages]","PDEBUGHOOKINFO","PDEBUGHOOKINFO structure pointer [Windows and Messages]","_win32_DEBUGHOOKINFO_str","_win32_debughookinfo_str_cpp","winmsg.debughookinfo","winui._win32_debughookinfo_str","winuser/DEBUGHOOKINFO","winuser/LPDEBUGHOOKINFO","winuser/PDEBUGHOOKINFO"]
old-location: winmsg\debughookinfo.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\hooks\hookreference\hookstructures\debughookinfo.htm
ms.date: 12/05/2018
ms.keywords: '*LPDEBUGHOOKINFO, *NPDEBUGHOOKINFO, *PDEBUGHOOKINFO, DEBUGHOOKINFO, DEBUGHOOKINFO structure [Windows and Messages], LPDEBUGHOOKINFO, LPDEBUGHOOKINFO structure pointer [Windows and Messages], PDEBUGHOOKINFO, PDEBUGHOOKINFO structure pointer [Windows and Messages], _win32_DEBUGHOOKINFO_str, _win32_debughookinfo_str_cpp, winmsg.debughookinfo, winui._win32_debughookinfo_str, winuser/DEBUGHOOKINFO, winuser/LPDEBUGHOOKINFO, winuser/PDEBUGHOOKINFO'
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
req.typenames: DEBUGHOOKINFO, *PDEBUGHOOKINFO, *NPDEBUGHOOKINFO, *LPDEBUGHOOKINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDEBUGHOOKINFO
 - winuser/tagDEBUGHOOKINFO
 - PDEBUGHOOKINFO
 - winuser/PDEBUGHOOKINFO
 - DEBUGHOOKINFO
 - winuser/DEBUGHOOKINFO
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
 - DEBUGHOOKINFO
---

# DEBUGHOOKINFO structure


## -description

Contains debugging information passed to a <b>WH_DEBUG</b> hook procedure, [*DebugProc*](/windows/win32/winmsg/debugproc).

## -struct-fields

### -field idThread

Type: <b>DWORD</b>

A handle to the thread containing the filter function.

### -field idThreadInstaller

Type: <b>DWORD</b>

A handle to the thread that installed the debugging filter function.

### -field lParam

Type: <b>LPARAM</b>

The value to be passed to the hook in the <i>lParam</i> parameter of the [*DebugProc*](/windows/win32/winmsg/debugproc) callback function.

### -field wParam

Type: <b>WPARAM</b>

The value to be passed to the hook in the <i>wParam</i> parameter of the [*DebugProc*](/windows/win32/winmsg/debugproc) callback function.

### -field code

Type: <b>int</b>

The value to be passed to the hook in the <i>nCode</i> parameter of the [*DebugProc*](/windows/win32/winmsg/debugproc) callback function.

## -see-also


[*DebugProc*](/windows/win32/winmsg/debugproc)


<a href="/windows/desktop/winmsg/hooks">Hooks</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setwindowshookexa">SetWindowsHookEx</a>