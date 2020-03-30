---
UID: NF:winuser.BeginDeferWindowPos
title: BeginDeferWindowPos function (winuser.h)
description: Allocates memory for a multiple-window- position structure and returns the handle to the structure.
old-location: winmsg\begindeferwindowpos.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\begindeferwindowpos.htm
ms.date: 12/05/2018
ms.keywords: BeginDeferWindowPos, BeginDeferWindowPos function [Windows and Messages], _win32_BeginDeferWindowPos, _win32_begindeferwindowpos_cpp, winmsg.begindeferwindowpos, winui._win32_begindeferwindowpos, winuser/BeginDeferWindowPos
f1_keywords:
- winuser/BeginDeferWindowPos
dev_langs:
- c++
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
- Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
api_name:
- BeginDeferWindowPos
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# BeginDeferWindowPos function


## -description


Allocates memory for a multiple-window- position structure and returns the handle to the structure. 


## -parameters




### -param nNumWindows [in]

Type: <b>int</b>

The initial number of windows for which to store position information. The <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-deferwindowpos">DeferWindowPos</a> function increases the size of the structure, if necessary. 


## -returns



Type: <b>HDWP</b>

If the function succeeds, the return value identifies the multiple-window-position structure. If insufficient system resources are available to allocate the structure, the return value is <b>NULL</b>. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



The multiple-window-position structure is an internal structure; an application cannot access it directly. 


<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-deferwindowpos">DeferWindowPos</a> fills the multiple-window-position structure with information about the target position for one or more windows about to be moved. The <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-enddeferwindowpos">EndDeferWindowPos</a> function accepts the handle to this structure and repositions the windows by using the information stored in the structure. 

If any of the windows in the multiple-window- position structure have the <b>SWP_HIDEWINDOW</b> or <b>SWP_SHOWWINDOW</b> flag set, none of the windows are repositioned.

If the system must increase the size of the multiple-window- position structure beyond the initial size specified by the <i>nNumWindows</i> parameter but cannot allocate enough memory to do so, the system fails the entire window positioning sequence (<b>BeginDeferWindowPos</b>, <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-deferwindowpos">DeferWindowPos</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-enddeferwindowpos">EndDeferWindowPos</a>). By specifying the maximum size needed, an application can detect and process failure early in the process. 




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-deferwindowpos">DeferWindowPos</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-enddeferwindowpos">EndDeferWindowPos</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setwindowpos">SetWindowPos</a>



<a href="https://docs.microsoft.com/windows/desktop/winmsg/windows">Windows</a>
 

 

