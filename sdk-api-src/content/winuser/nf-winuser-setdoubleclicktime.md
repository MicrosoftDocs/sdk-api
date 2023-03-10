---
UID: NF:winuser.SetDoubleClickTime
title: SetDoubleClickTime function (winuser.h)
description: Sets the double-click time for the mouse.
helpviewer_keywords: ["SetDoubleClickTime","SetDoubleClickTime function [Keyboard and Mouse Input]","_win32_SetDoubleClickTime","_win32_setdoubleclicktime_cpp","inputdev.setdoubleclicktime","winui._win32_setdoubleclicktime","winuser/SetDoubleClickTime"]
old-location: inputdev\setdoubleclicktime.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\mouseinput\mouseinputreference\mouseinputfunctions\setdoubleclicktime.htm
ms.date: 12/05/2018
ms.keywords: SetDoubleClickTime, SetDoubleClickTime function [Keyboard and Mouse Input], _win32_SetDoubleClickTime, _win32_setdoubleclicktime_cpp, inputdev.setdoubleclicktime, winui._win32_setdoubleclicktime, winuser/SetDoubleClickTime
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetDoubleClickTime
 - winuser/SetDoubleClickTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - SetDoubleClickTime
req.apiset: ext-ms-win-ntuser-mouse-l1-1-1 (introduced in Windows 10, version 10.0.14393)
---

# SetDoubleClickTime function


## -description

Sets the double-click time for the mouse. A double-click is a series of two clicks of a mouse button, the second occurring within a specified time after the first. The double-click time is the maximum number of milliseconds that may occur between the first and second clicks of a double-click.

## -parameters

### -param unnamedParam1 [in]

Type: <b>UINT</b>

The number of milliseconds that may occur between the first and second clicks of a double-click. If this parameter is set to 0, the system uses the default double-click time of 500 milliseconds. If this parameter value is greater than 5000 milliseconds, the system sets the value to 5000 milliseconds.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>SetDoubleClickTime</b> function alters the double-click time for all windows in the system.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime">GetDoubleClickTime</a>



<a href="/windows/desktop/inputdev/mouse-input">Mouse Input</a>



<b>Reference</b>
