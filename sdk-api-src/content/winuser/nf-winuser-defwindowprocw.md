---
UID: NF:winuser.DefWindowProcW
title: DefWindowProcW function
author: windows-sdk-content
description: Calls the default window procedure to provide default processing for any window messages that an application does not process.
old-location: winmsg\defwindowproc.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowprocedures\windowprocedurereference\windowprocedurefunctions\defwindowproc.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: DefWindowProc, DefWindowProc function [Windows and Messages], DefWindowProcA, DefWindowProcW, _win32_DefWindowProc, _win32_defwindowproc_cpp, winmsg.defwindowproc, winui._win32_defwindowproc, winuser/DefWindowProc, winuser/DefWindowProcA, winuser/DefWindowProcW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DefWindowProcW (Unicode) and DefWindowProcA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - API-MS-Win-NTUser-IE-Window-l1-1-0.dll
 - ie_shims.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - DefWindowProc
 - DefWindowProcA
 - DefWindowProcW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- DefWindowProcW
: 
---

# DefWindowProcW function


## -description


Calls the default window procedure to provide default processing for any window messages that an application does not process. This function ensures that every message is processed. <b>DefWindowProc</b> is called with the same parameters received by the window procedure. 


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window procedure that received the message. 


### -param Msg [in]

Type: <b>UINT</b>

The message. 


### -param wParam [in]

Type: <b>WPARAM</b>

Additional message information. The content of this parameter depends on the value of the <i>Msg</i> parameter. 


### -param lParam [in]

Type: <b>LPARAM</b>

Additional message information. The content of this parameter depends on the value of the <i>Msg</i> parameter. 


## -returns



Type: <strong>Type: <b>LRESULT</b>
</strong>

The return value is the result of the message processing and depends on the message. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms633571(v=VS.85).aspx">CallWindowProc</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms645450(v=VS.85).aspx">DefDlgProc</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms632593(v=VS.85).aspx">Window Procedures</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633573(v=VS.85).aspx">WindowProc</a>
 

 

