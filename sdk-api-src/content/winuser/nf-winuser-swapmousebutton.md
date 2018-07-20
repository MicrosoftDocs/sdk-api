---
UID: NF:winuser.SwapMouseButton
title: SwapMouseButton function
author: windows-sdk-content
description: Reverses or restores the meaning of the left and right mouse buttons.
old-location: inputdev\swapmousebutton.htm
old-project: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\mouseinput\mouseinputreference\mouseinputfunctions\swapmousebutton.htm
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: SwapMouseButton, SwapMouseButton function [Keyboard and Mouse Input], _win32_SwapMouseButton, _win32_swapmousebutton_cpp, inputdev.swapmousebutton, winui._win32_swapmousebutton, winuser/SwapMouseButton
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
 - SwapMouseButton
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SwapMouseButton function


## -description


Reverses or restores the meaning of the left and right mouse buttons. 


## -parameters




### -param fSwap [in]

Type: <b>BOOL</b>

If this parameter is <b>TRUE</b>, the left button generates right-button messages and the right button generates left-button messages. If this parameter is <b>FALSE</b>, the buttons are restored to their original meanings. 


## -returns



Type: <b>BOOL</b>

If the meaning of the mouse buttons was reversed previously, before the function was called, the return value is nonzero.

If the meaning of the mouse buttons was not reversed, the return value is zero. 




## -remarks



Button swapping is provided as a convenience to people who use the mouse with their left hands. The <b>SwapMouseButton</b> function is usually called by Control Panel only. Although an application is free to call the function, the mouse is a shared resource and reversing the meaning of its buttons affects all applications. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/library/ms645533(v=VS.85).aspx">Mouse Input</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/ms646263(v=VS.85).aspx">SetDoubleClickTime</a>
 

 

