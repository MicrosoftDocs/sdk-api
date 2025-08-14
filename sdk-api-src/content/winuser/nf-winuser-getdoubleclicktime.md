---
UID: NF:winuser.GetDoubleClickTime
title: GetDoubleClickTime function (winuser.h)
description: Retrieves the current double-click time for the mouse.
helpviewer_keywords: ["GetDoubleClickTime","GetDoubleClickTime function [Keyboard and Mouse Input]","_win32_GetDoubleClickTime","_win32_getdoubleclicktime_cpp","inputdev.getdoubleclicktime","winui._win32_getdoubleclicktime","winuser/GetDoubleClickTime"]
old-location: inputdev\getdoubleclicktime.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\mouseinput\mouseinputreference\mouseinputfunctions\getdoubleclicktime.htm
ms.date: 12/05/2018
ms.keywords: GetDoubleClickTime, GetDoubleClickTime function [Keyboard and Mouse Input], _win32_GetDoubleClickTime, _win32_getdoubleclicktime_cpp, inputdev.getdoubleclicktime, winui._win32_getdoubleclicktime, winuser/GetDoubleClickTime
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
 - GetDoubleClickTime
 - winuser/GetDoubleClickTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-mouse-l1-1-0.dll
 - ext-ms-win-ntuser-mouse-l1-1-1.dll
 - User32.dll
 - Ext-MS-Win-NTUser-mouse-l1-1-0.dll
 - api-ms-win-ntuser-ie-mouse-l1-1-0.dll
 - ie_stubs.dll
api_name:
 - GetDoubleClickTime
req.apiset: ext-ms-win-ntuser-mouse-l1-1-0 (introduced in Windows 8)
---

# GetDoubleClickTime function


## -description

Retrieves the current double-click time for the mouse. A double-click is a series of two clicks of the mouse button, the second occurring within a specified time after the first. The double-click time is the maximum number of milliseconds that may occur between the first and second click of a double-click. The maximum double-click time is 5000 milliseconds.



## -returns

Type: <b>UINT</b>

The return value specifies the current double-click time, in milliseconds. The maximum return value is 5000 milliseconds.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/inputdev/mouse-input">Mouse Input</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setdoubleclicktime">SetDoubleClickTime</a>
