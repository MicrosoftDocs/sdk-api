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


Processes accelerator keystrokes for window menu commands of the multiple-document interface (MDI) child windows associated with the specified MDI client window. The function translates <a href="https://msdn.microsoft.com/67d9d82d-fab0-4aec-a337-7a9cb2b0b586">WM_KEYUP</a> and <a href="https://msdn.microsoft.com/0e37149f-445c-4b20-ad68-fdf39428ac91">WM_KEYDOWN</a> messages to <a href="https://msdn.microsoft.com/82c7cc95-82d5-4f0f-8c78-ab325561b04e">WM_SYSCOMMAND</a> messages and sends them to the appropriate MDI child windows. 


## -parameters




### -param hWndClient [in]

Type: <b>HWND</b>

A handle to the MDI client window. 


### -param lpMsg [in]

Type: <b>LPMSG</b>

A pointer to a message retrieved by using the <a href="https://msdn.microsoft.com/e92266a7-86ac-43f4-b0eb-762e145a1017">GetMessage</a> or <a href="https://msdn.microsoft.com/b9f5baa4-8166-4d6e-b416-df023aed9bad">PeekMessage</a> function. The message must be an <a href="https://msdn.microsoft.com/fee176ba-ad07-4145-ab4d-1b8c335fd100">MSG</a> structure and contain message information from the application's message queue. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the message is translated into a system command, the return value is nonzero.

If the message is not translated into a system command, the return value is zero.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/e92266a7-86ac-43f4-b0eb-762e145a1017">GetMessage</a>



<a href="https://msdn.microsoft.com/fee176ba-ad07-4145-ab4d-1b8c335fd100">MSG</a>



<a href="https://msdn.microsoft.com/beb41067-91ed-4f63-af8f-1000ba82a3b1">Multiple Document Interface</a>



<a href="https://msdn.microsoft.com/b9f5baa4-8166-4d6e-b416-df023aed9bad">PeekMessage</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/0d8a970c-68b2-45e6-8702-2490029c1e1d">TranslateAccelerator</a>



<a href="https://msdn.microsoft.com/0e37149f-445c-4b20-ad68-fdf39428ac91">WM_KEYDOWN</a>



<a href="https://msdn.microsoft.com/67d9d82d-fab0-4aec-a337-7a9cb2b0b586">WM_KEYUP</a>



<a href="https://msdn.microsoft.com/82c7cc95-82d5-4f0f-8c78-ab325561b04e">WM_SYSCOMMAND</a>
 

 

