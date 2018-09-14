---
UID: NF:winuser.SetDoubleClickTime
title: SetDoubleClickTime function
author: windows-sdk-content
description: Sets the double-click time for the mouse.
old-location: inputdev\setdoubleclicktime.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\mouseinput\mouseinputreference\mouseinputfunctions\setdoubleclicktime.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: SetDoubleClickTime, SetDoubleClickTime function [Keyboard and Mouse Input], _win32_SetDoubleClickTime, _win32_setdoubleclicktime_cpp, inputdev.setdoubleclicktime, winui._win32_setdoubleclicktime, winuser/SetDoubleClickTime
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
 - SetDoubleClickTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetDoubleClickTime function


## -description


Sets the double-click time for the mouse. A double-click is a series of two clicks of a mouse button, the second occurring within a specified time after the first. The double-click time is the maximum number of milliseconds that may occur between the first and second clicks of a double-click. 


## -parameters




### -param Arg1 [in]

Type: <b>UINT</b>

The number of milliseconds that may occur between the first and second clicks of a double-click. If this parameter is set to 0, the system uses the default double-click time of 500 milliseconds. If this parameter value is greater than 5000 milliseconds, the system sets the value to 5000 milliseconds.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.





## -remarks



The <b>SetDoubleClickTime</b> function alters the double-click time for all windows in the system. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/8917bc74-d925-4f67-af5c-ab8fe6ad9607">GetDoubleClickTime</a>



<a href="https://msdn.microsoft.com/35f5e1ad-74d5-41bb-9016-b1c5de449550">Mouse Input</a>



<b>Reference</b>
 

 

