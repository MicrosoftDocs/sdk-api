---
UID: NF:winuser.DefFrameProcA
title: DefFrameProcA function
author: windows-sdk-content
description: Provides default processing for any window messages that the window procedure of a multiple-document interface (MDI) frame window does not process.
old-location: winmsg\defframeproc.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\multipledocumentinterface\multipledocumentinterfacereference\multipledocumentinterfacefunctions\defframeproc.htm
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: DefFrameProc, DefFrameProc function [Windows and Messages], DefFrameProcA, DefFrameProcW, _win32_DefFrameProc, _win32_defframeproc_cpp, winmsg.defframeproc, winui._win32_defframeproc, winuser/DefFrameProc, winuser/DefFrameProcA, winuser/DefFrameProcW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DefFrameProcW (Unicode) and DefFrameProcA (ANSI)
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
 - DefFrameProc
 - DefFrameProcA
 - DefFrameProcW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# DefFrameProcA function


## -description


Provides default processing for any window messages that the window procedure of a multiple-document interface (MDI) frame window does not process. All window messages that are not explicitly processed by the window procedure must be passed to the <b>DefFrameProc</b> function, not the <a href="https://msdn.microsoft.com/fcc6b242-e152-4364-a977-b0441bec425f">DefWindowProc</a> function. 


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the MDI frame window. 


### -param hWndMDIClient [in]

Type: <b>HWND</b>

A handle to the MDI client window. 


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

The return value specifies the result of the message processing and depends on the message. If the <i>hWndMDIClient</i> parameter is <b>NULL</b>, the return value is the same as for the <a href="https://msdn.microsoft.com/fcc6b242-e152-4364-a977-b0441bec425f">DefWindowProc</a> function. 




## -remarks



When an application's window procedure does not handle a message, it typically passes the message to the <a href="https://msdn.microsoft.com/fcc6b242-e152-4364-a977-b0441bec425f">DefWindowProc</a> function to process the message. MDI applications use the <b>DefFrameProc</b> and <a href="https://msdn.microsoft.com/be5ba88e-2d7a-4552-a16e-180637ca7af7">DefMDIChildProc</a> functions instead of <b>DefWindowProc</b> to provide default message processing. All messages that an application would usually pass to <b>DefWindowProc</b> (such as nonclient messages and the <a href="https://msdn.microsoft.com/1b48c309-6903-4139-bf42-e8526963e681">WM_SETTEXT</a> message) should be passed to <b>DefFrameProc</b> instead. The <b>DefFrameProc</b> function also handles the following messages. 

				

<table class="clsStd">
<tr>
<th>Message</th>
<th>Response</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/5516098e-fd90-49c8-afb0-78164b028376">WM_COMMAND</a>
</td>
<td>Activates the MDI child window that the user chooses. This message is sent when the user chooses an MDI child window from the window menu of the MDI frame window. The window identifier accompanying this message identifies the MDI child window to be activated.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/de6c91bb-80fd-44b2-8d96-d016477a6547">WM_MENUCHAR</a>
</td>
<td>Opens the window menu of the active MDI child window when the user presses the ALT+ – (minus) key combination.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/77180e4c-95a6-41a4-93d9-033381ae7543">WM_SETFOCUS</a>
</td>
<td>Passes the keyboard focus to the MDI client window, which in turn passes it to the active MDI child window.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/e3e14dcd-9236-48bd-a692-6985d8146f81">WM_SIZE</a>
</td>
<td>Resizes the MDI client window to fit in the new frame window's client area. If the frame window procedure sizes the MDI client window to a different size, it should not pass the message to the <a href="https://msdn.microsoft.com/fcc6b242-e152-4364-a977-b0441bec425f">DefWindowProc</a> function.</td>
</tr>
</table>
 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/be5ba88e-2d7a-4552-a16e-180637ca7af7">DefMDIChildProc</a>



<a href="https://msdn.microsoft.com/fcc6b242-e152-4364-a977-b0441bec425f">DefWindowProc</a>



<a href="https://msdn.microsoft.com/beb41067-91ed-4f63-af8f-1000ba82a3b1">Multiple Document Interface</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/1b48c309-6903-4139-bf42-e8526963e681">WM_SETTEXT</a>
 

 

