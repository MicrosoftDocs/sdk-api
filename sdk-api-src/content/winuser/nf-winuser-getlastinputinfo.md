---
UID: NF:winuser.GetLastInputInfo
title: GetLastInputInfo function (winuser.h)
description: Retrieves the time of the last input event.
helpviewer_keywords: ["GetLastInputInfo","GetLastInputInfo function [Keyboard and Mouse Input]","_win32_GetLastInputInfo","_win32_getlastinputinfo_cpp","inputdev.getlastinputinfo","winui._win32_getlastinputinfo","winuser/GetLastInputInfo"]
old-location: inputdev\getlastinputinfo.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\getlastinputinfo.htm
ms.date: 12/05/2018
ms.keywords: GetLastInputInfo, GetLastInputInfo function [Keyboard and Mouse Input], _win32_GetLastInputInfo, _win32_getlastinputinfo_cpp, inputdev.getlastinputinfo, winui._win32_getlastinputinfo, winuser/GetLastInputInfo
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
 - GetLastInputInfo
 - winuser/GetLastInputInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-keyboard-l1-3-2.dll
 - ext-ms-win-ntuser-keyboard-l1-3-1.dll
 - User32.dll
 - Ext-MS-Win-NTUser-Keyboard-l1-1-0.dll
 - Ext-MS-Win-NTUser-Keyboard-l1-1-1.dll
 - ext-ms-win-ntuser-keyboard-l1-1-2.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-0.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-1.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-3-0.dll
api_name:
 - GetLastInputInfo
---

# GetLastInputInfo function


## -description

Retrieves the time of the last input event.

## -parameters

### -param plii [out]

Type: <b>PLASTINPUTINFO</b>

A pointer to a <a href="/windows/desktop/api/winuser/ns-winuser-lastinputinfo">LASTINPUTINFO</a> structure that receives the time of the last input event.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

This function is useful for input idle detection. However, <b>GetLastInputInfo</b> does not provide system-wide user input information across all running sessions. Rather, <b>GetLastInputInfo</b> provides session-specific user input information for only the session that invoked the function.

The tick count when the last input event was received (see <a href="/windows/desktop/api/winuser/ns-winuser-lastinputinfo">LASTINPUTINFO</a>) is not guaranteed to be incremental. In some cases, the value might be less than the tick count of a prior event. For example, this can be caused by a timing gap between the raw input thread and the desktop thread or an event raised by <a href="/windows/desktop/api/winuser/nf-winuser-sendinput">SendInput</a>, which supplies its own tick count.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/inputdev/keyboard-input">Keyboard Input</a>



<a href="/windows/desktop/api/winuser/ns-winuser-lastinputinfo">LASTINPUTINFO</a>



<b>Reference</b>