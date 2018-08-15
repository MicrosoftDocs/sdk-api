---
UID: NF:winuser.EndTask
title: EndTask function
author: windows-sdk-content
description: Forcibly closes the specified window.
old-location: winmsg\endtask.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\endtask.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: EndTask, EndTask function [Windows and Messages], _win32_EndTask, _win32_endtask_cpp, winmsg.endtask, winui._win32_endtask, winuser/EndTask
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
req.unicode-ansi: 
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
 - EndTask
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# EndTask function


## -description


<p class="CCE_Message">[This function is not intended for general
      use. It may
      be altered or unavailable in subsequent versions of Windows.]

Forcibly closes the
		specified window. 


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window to be closed. 


### -param fShutDown [in]

Type: <b>BOOL</b>

Ignored. Must be <b>FALSE</b>. 


### -param fForce [in]

Type: <b>BOOL</b>

A <b>TRUE</b> for this parameter will force the destruction of the
        window if an initial attempt fails to gently close the window using <a href="https://msdn.microsoft.com/en-us/library/ms632617(v=VS.85).aspx">WM_CLOSE</a>.
        With a <b>FALSE</b> for this parameter, only the close with <b>WM_CLOSE</b>is attempted. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is <b>FALSE</b>.
				To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



This function was not included in the SDK headers and libraries until Windows XP with Service Pack 1 (SP1) and Windows Server 2003. If you do not have a header file and import library for this function, you can call the function using <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms632678(v=VS.85).aspx">CloseWindow</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms632682(v=VS.85).aspx">DestroyWindow</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms632617(v=VS.85).aspx">WM_CLOSE</a>



<a href="https://msdn.microsoft.com/e2c778c7-7319-4bf7-a6a7-b526e4f3e98b">Windows</a>
 

 

