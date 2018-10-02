---
UID: NS:winuser.tagDEBUGHOOKINFO
title: tagDEBUGHOOKINFO
author: windows-sdk-content
description: Contains debugging information passed to a WH_DEBUG hook procedure, DebugProc.
old-location: winmsg\debughookinfo.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\hooks\hookreference\hookstructures\debughookinfo.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*LPDEBUGHOOKINFO, *NPDEBUGHOOKINFO, *PDEBUGHOOKINFO, DEBUGHOOKINFO, DEBUGHOOKINFO structure [Windows and Messages], LPDEBUGHOOKINFO, LPDEBUGHOOKINFO structure pointer [Windows and Messages], PDEBUGHOOKINFO, PDEBUGHOOKINFO structure pointer [Windows and Messages], _win32_DEBUGHOOKINFO_str, _win32_debughookinfo_str_cpp, tagDEBUGHOOKINFO, winmsg.debughookinfo, winui._win32_debughookinfo_str, winuser/DEBUGHOOKINFO, winuser/LPDEBUGHOOKINFO, winuser/PDEBUGHOOKINFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - DEBUGHOOKINFO
product: Windows
targetos: Windows
req.typenames: DEBUGHOOKINFO, *PDEBUGHOOKINFO, *NPDEBUGHOOKINFO, *LPDEBUGHOOKINFO
req.redist: 
---

# tagDEBUGHOOKINFO structure


## -description


Contains debugging information passed to a <b>WH_DEBUG</b> hook procedure, <a href="https://msdn.microsoft.com/en-us/library/ms644978(v=VS.85).aspx">DebugProc</a>. 


## -struct-fields




### -field idThread

Type: <b>DWORD</b>

A handle to the thread containing the filter function. 


### -field idThreadInstaller

Type: <b>DWORD</b>

A handle to the thread that installed the debugging filter function. 


### -field lParam

Type: <b>LPARAM</b>

The value to be passed to the hook in the 
					<i>lParam</i> parameter of the <a href="https://msdn.microsoft.com/en-us/library/ms644978(v=VS.85).aspx">DebugProc</a> callback function. 


### -field wParam

Type: <b>WPARAM</b>

The value to be passed to the hook in the 
					<i>wParam</i> parameter of the <a href="https://msdn.microsoft.com/en-us/library/ms644978(v=VS.85).aspx">DebugProc</a> callback function. 


### -field code

Type: <b>int</b>

The value to be passed to the hook in the 
					<i>nCode</i> parameter of the <a href="https://msdn.microsoft.com/en-us/library/ms644978(v=VS.85).aspx">DebugProc</a> callback function. 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms644978(v=VS.85).aspx">DebugProc</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632589(v=VS.85).aspx">Hooks</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms644990(v=VS.85).aspx">SetWindowsHookEx</a>
 

 

