---
UID: NF:winuser.DefMDIChildProcW
title: DefMDIChildProcW function
author: windows-sdk-content
description: Provides default processing for any window message that the window procedure of a multiple-document interface (MDI) child window does not process.
old-location: winmsg\defmdichildproc.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\multipledocumentinterface\multipledocumentinterfacereference\multipledocumentinterfacefunctions\defmdichildproc.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: DefMDIChildProc, DefMDIChildProc function [Windows and Messages], DefMDIChildProcA, DefMDIChildProcW, _win32_DefMDIChildProc, _win32_defmdichildproc_cpp, winmsg.defmdichildproc, winui._win32_defmdichildproc, winuser/DefMDIChildProc, winuser/DefMDIChildProcA, winuser/DefMDIChildProcW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DefMDIChildProcW (Unicode) and DefMDIChildProcA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - DefMDIChildProc
 - DefMDIChildProcA
 - DefMDIChildProcW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# DefMDIChildProcW function


## -description


Provides default processing for any window message that the window procedure of a multiple-document interface (MDI) child window does not process. A window message not processed by the window procedure must be passed to the <b>DefMDIChildProc</b> function, not to the <a href="https://msdn.microsoft.com/fcc6b242-e152-4364-a977-b0441bec425f">DefWindowProc</a> function. 


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the MDI child window. 


### -param uMsg [in]

Type: <b>UINT</b>

The message to be processed. 


### -param wParam [in]

Type: <b>WPARAM</b>

Additional message-specific information. 


### -param lParam [in]

Type: <b>LPARAM</b>

Additional message-specific information. 


## -returns



Type: <strong>Type: <b>LRESULT</b>
</strong>

The return value specifies the result of the message processing and depends on the message. 




## -remarks



The <b>DefMDIChildProc</b> function assumes that the parent window of the MDI child window identified by the <i>hWnd</i> parameter was created with the <b>MDICLIENT</b> class. 

When an application's window procedure does not handle a message, it typically passes the message to the <a href="https://msdn.microsoft.com/fcc6b242-e152-4364-a977-b0441bec425f">DefWindowProc</a> function to process the message. MDI applications use the <a href="https://msdn.microsoft.com/6ac25af4-dd93-43f6-83b0-a49f42761a29">DefFrameProc</a> and <b>DefMDIChildProc</b> functions instead of <b>DefWindowProc</b> to provide default message processing. All messages that an application would usually pass to <b>DefWindowProc</b> (such as nonclient messages and the <a href="https://msdn.microsoft.com/1b48c309-6903-4139-bf42-e8526963e681">WM_SETTEXT</a> message) should be passed to <b>DefMDIChildProc</b> instead. In addition, <b>DefMDIChildProc</b> also handles the following messages. 

				

<table class="clsStd">
<tr>
<th>Message</th>
<th>Response</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/6e60725d-aa01-48bb-86a5-f17f56b97d35">WM_CHILDACTIVATE</a>
</td>
<td>Performs activation processing when MDI child windows are sized, moved, or displayed. This message must be passed.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/af2295e0-2d0b-4ac0-b689-16138022f4b7">WM_GETMINMAXINFO</a>
</td>
<td>Calculates the size of a maximized MDI child window, based on the current size of the MDI client window.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/de6c91bb-80fd-44b2-8d96-d016477a6547">WM_MENUCHAR</a>
</td>
<td>Passes the message to the MDI frame window.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/552ddc26-fe63-449b-8c82-bb927a2c1c41">WM_MOVE</a>
</td>
<td>Recalculates MDI client scroll bars if they are present.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/77180e4c-95a6-41a4-93d9-033381ae7543">WM_SETFOCUS</a>
</td>
<td>Activates the child window if it is not the active MDI child window.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/e3e14dcd-9236-48bd-a692-6985d8146f81">WM_SIZE</a>
</td>
<td>Performs operations necessary for changing the size of a window, especially for maximizing or restoring an MDI child window. Failing to pass this message to the <b>DefMDIChildProc</b> function produces highly undesirable results.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/82c7cc95-82d5-4f0f-8c78-ab325561b04e">WM_SYSCOMMAND</a>
</td>
<td>Handles window menu commands: <b>SC_NEXTWINDOW</b>, <b>SC_PREVWINDOW</b>, <b>SC_MOVE</b>, <b>SC_SIZE</b>, and <b>SC_MAXIMIZE</b>.</td>
</tr>
</table>
 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/6ac25af4-dd93-43f6-83b0-a49f42761a29">DefFrameProc</a>



<a href="https://msdn.microsoft.com/fcc6b242-e152-4364-a977-b0441bec425f">DefWindowProc</a>



<a href="https://msdn.microsoft.com/beb41067-91ed-4f63-af8f-1000ba82a3b1">Multiple Document Interface</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/6e60725d-aa01-48bb-86a5-f17f56b97d35">WM_CHILDACTIVATE</a>



<a href="https://msdn.microsoft.com/af2295e0-2d0b-4ac0-b689-16138022f4b7">WM_GETMINMAXINFO</a>



<a href="https://msdn.microsoft.com/de6c91bb-80fd-44b2-8d96-d016477a6547">WM_MENUCHAR</a>



<a href="https://msdn.microsoft.com/552ddc26-fe63-449b-8c82-bb927a2c1c41">WM_MOVE</a>



<a href="https://msdn.microsoft.com/77180e4c-95a6-41a4-93d9-033381ae7543">WM_SETFOCUS</a>



<a href="https://msdn.microsoft.com/1b48c309-6903-4139-bf42-e8526963e681">WM_SETTEXT</a>



<a href="https://msdn.microsoft.com/e3e14dcd-9236-48bd-a692-6985d8146f81">WM_SIZE</a>



<a href="https://msdn.microsoft.com/82c7cc95-82d5-4f0f-8c78-ab325561b04e">WM_SYSCOMMAND</a>
 

 

