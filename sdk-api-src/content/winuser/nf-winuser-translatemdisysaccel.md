---
UID: NF:winuser.TranslateMDISysAccel
title: TranslateMDISysAccel function
author: windows-sdk-content
description: Processes accelerator keystrokes for window menu commands of the multiple-document interface (MDI) child windows associated with the specified MDI client window.
old-location: winmsg\translatemdisysaccel.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\multipledocumentinterface\multipledocumentinterfacereference\multipledocumentinterfacefunctions\translatemdisysaccel.htm
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: TranslateMDISysAccel, TranslateMDISysAccel function [Windows and Messages], _win32_TranslateMDISysAccel, _win32_translatemdisysaccel_cpp, winmsg.translatemdisysaccel, winui._win32_translatemdisysaccel, winuser/TranslateMDISysAccel
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
api_name:
 - TranslateMDISysAccel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- TranslateMDISysAccel
: 
---

# TranslateMDISysAccel function


## -description


Processes accelerator keystrokes for window menu commands of the multiple-document interface (MDI) child windows associated with the specified MDI client window. The function translates <a href="https://msdn.microsoft.com/en-us/library/ms646281(v=VS.85).aspx">WM_KEYUP</a> and <a href="https://msdn.microsoft.com/en-us/library/ms646280(v=VS.85).aspx">WM_KEYDOWN</a> messages to <a href="https://msdn.microsoft.com/en-us/library/ms646360(v=VS.85).aspx">WM_SYSCOMMAND</a> messages and sends them to the appropriate MDI child windows. 


## -parameters




### -param hWndClient [in]

Type: <b>HWND</b>

A handle to the MDI client window. 


### -param lpMsg [in]

Type: <b>LPMSG</b>

A pointer to a message retrieved by using the <a href="https://msdn.microsoft.com/en-us/library/ms644936(v=VS.85).aspx">GetMessage</a> or <a href="https://msdn.microsoft.com/en-us/library/ms644943(v=VS.85).aspx">PeekMessage</a> function. The message must be an <a href="https://msdn.microsoft.com/en-us/library/ms644958(v=VS.85).aspx">MSG</a> structure and contain message information from the application's message queue. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the message is translated into a system command, the return value is nonzero.

If the message is not translated into a system command, the return value is zero.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms644936(v=VS.85).aspx">GetMessage</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644958(v=VS.85).aspx">MSG</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632591(v=VS.85).aspx">Multiple Document Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644943(v=VS.85).aspx">PeekMessage</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646373(v=VS.85).aspx">TranslateAccelerator</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646280(v=VS.85).aspx">WM_KEYDOWN</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646281(v=VS.85).aspx">WM_KEYUP</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646360(v=VS.85).aspx">WM_SYSCOMMAND</a>
 

 

