---
UID: NF:winuser.BeginDeferWindowPos
title: BeginDeferWindowPos function
author: windows-sdk-content
description: Allocates memory for a multiple-window- position structure and returns the handle to the structure.
old-location: winmsg\begindeferwindowpos.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\begindeferwindowpos.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: BeginDeferWindowPos, BeginDeferWindowPos function [Windows and Messages], _win32_BeginDeferWindowPos, _win32_begindeferwindowpos_cpp, winmsg.begindeferwindowpos, winui._win32_begindeferwindowpos, winuser/BeginDeferWindowPos
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BeginDeferWindowPos function


## -description


Allocates memory for a multiple-window- position structure and returns the handle to the structure. 


## -parameters




### -param nNumWindows [in]

Type: <b>int</b>

The initial number of windows for which to store position information. The <a href="https://msdn.microsoft.com/en-us/library/ms632681(v=VS.85).aspx">DeferWindowPos</a> function increases the size of the structure, if necessary. 


## -returns



Type: <strong>Type: <b>HDWP</b>
</strong>

If the function succeeds, the return value identifies the multiple-window-position structure. If insufficient system resources are available to allocate the structure, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The multiple-window-position structure is an internal structure; an application cannot access it directly. 


<a href="https://msdn.microsoft.com/en-us/library/ms632681(v=VS.85).aspx">DeferWindowPos</a> fills the multiple-window-position structure with information about the target position for one or more windows about to be moved. The <a href="https://msdn.microsoft.com/en-us/library/ms633440(v=VS.85).aspx">EndDeferWindowPos</a> function accepts the handle to this structure and repositions the windows by using the information stored in the structure. 

If any of the windows in the multiple-window- position structure have the <b>SWP_HIDEWINDOW</b> or <b>SWP_SHOWWINDOW</b> flag set, none of the windows are repositioned.

If the system must increase the size of the multiple-window- position structure beyond the initial size specified by the <i>nNumWindows</i> parameter but cannot allocate enough memory to do so, the system fails the entire window positioning sequence (<b>BeginDeferWindowPos</b>, <a href="https://msdn.microsoft.com/en-us/library/ms632681(v=VS.85).aspx">DeferWindowPos</a>, and <a href="https://msdn.microsoft.com/en-us/library/ms633440(v=VS.85).aspx">EndDeferWindowPos</a>). By specifying the maximum size needed, an application can detect and process failure early in the process. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms632681(v=VS.85).aspx">DeferWindowPos</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633440(v=VS.85).aspx">EndDeferWindowPos</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633545(v=VS.85).aspx">SetWindowPos</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632595(v=VS.85).aspx">Windows</a>
 

 

