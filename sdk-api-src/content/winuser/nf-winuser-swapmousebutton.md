---
UID: NF:winuser.SwapMouseButton
title: SwapMouseButton function
author: windows-sdk-content
description: Reverses or restores the meaning of the left and right mouse buttons.
old-location: inputdev\swapmousebutton.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\mouseinput\mouseinputreference\mouseinputfunctions\swapmousebutton.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: SwapMouseButton, SwapMouseButton function [Keyboard and Mouse Input], _win32_SwapMouseButton, _win32_swapmousebutton_cpp, inputdev.swapmousebutton, winui._win32_swapmousebutton, winuser/SwapMouseButton
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
 - SwapMouseButton
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- SwapMouseButton
: 
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



<a href="https://msdn.microsoft.com/35f5e1ad-74d5-41bb-9016-b1c5de449550">Mouse Input</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/02d5d9ba-99eb-4853-94a1-7c203b5d3620">SetDoubleClickTime</a>
 

 

