---
UID: NF:winuser.DragDetect
title: DragDetect function
author: windows-sdk-content
description: Captures the mouse and tracks its movement until the user releases the left button, presses the ESC key, or moves the mouse outside the drag rectangle around the specified point.
old-location: inputdev\dragdetect.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\mouseinput\mouseinputreference\mouseinputfunctions\dragdetect.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DragDetect, DragDetect function [Keyboard and Mouse Input], _win32_DragDetect, _win32_dragdetect_cpp, inputdev.dragdetect, winui._win32_dragdetect, winuser/DragDetect
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
 - DragDetect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DragDetect function


## -description


Captures the mouse and tracks its movement until the user releases the left button, presses the ESC key, or moves the mouse outside the drag rectangle around the specified point. The width and height of the drag rectangle are specified by the <b>SM_CXDRAG</b> and <b>SM_CYDRAG</b> values returned by the <a href="https://msdn.microsoft.com/d063857b-6036-4e68-80af-9c70d12ae29e">GetSystemMetrics</a> function.


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

A handle to the window receiving mouse input. 


### -param pt [in]

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a></b>

Initial position of the mouse, in screen coordinates. The function determines the coordinates of the drag rectangle by using this point. 


## -returns



Type: <b>BOOL</b>

If the user moved the mouse outside of the drag rectangle while holding down the left button, the return value is nonzero.

If the user did not move the mouse outside of the drag rectangle while holding down the left button, the return value is zero.




## -remarks



The system metrics for the drag rectangle are configurable, allowing for larger or smaller drag rectangles. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/d063857b-6036-4e68-80af-9c70d12ae29e">GetSystemMetrics</a>



<a href="https://msdn.microsoft.com/35f5e1ad-74d5-41bb-9016-b1c5de449550">Mouse Input</a>



<a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>



<b>Reference</b>
 

 

