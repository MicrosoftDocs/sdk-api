---
UID: NF:winuser.FindWindowW
title: FindWindowW function (winuser.h)
description: Retrieves a handle to the top-level window whose class name and window name match the specified strings. This function does not search child windows. This function does not perform a case-sensitive search. (Unicode)
helpviewer_keywords: ["FindWindow", "FindWindow function [Windows and Messages]", "FindWindowW", "_win32_FindWindow", "_win32_findwindow_cpp", "winmsg.findwindow", "winui._win32_findwindow", "winuser/FindWindow", "winuser/FindWindowW"]
old-location: winmsg\findwindow.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\findwindow.htm
ms.date: 12/05/2018
ms.keywords: FindWindow, FindWindow function [Windows and Messages], FindWindowA, FindWindowW, _win32_FindWindow, _win32_findwindow_cpp, winmsg.findwindow, winui._win32_findwindow, winuser/FindWindow, winuser/FindWindowA, winuser/FindWindowW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FindWindowW (Unicode) and FindWindowA (ANSI)
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
 - FindWindowW
 - winuser/FindWindowW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-window-ext-l1-1-1.dll
 - ext-ms-win-ntuser-window-l1-1-6.dll
 - ext-ms-win-ntuser-window-l1-1-5.dll
 - User32.dll
 - API-MS-Win-NTUser-IE-Window-l1-1-0.dll
 - ie_shims.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - FindWindow
 - FindWindowA
 - FindWindowW
req.apiset: ext-ms-win-ntuser-window-l1-1-0 (introduced in Windows 8)
---

# FindWindowW function


## -description

Retrieves a handle to the top-level window whose class name and window name match the specified strings. This function does not search child windows. This function does not perform a case-sensitive search.

To search child windows, beginning with a specified child window, use the <a href="/windows/desktop/api/winuser/nf-winuser-findwindowexa">FindWindowEx</a> function.

## -parameters

### -param lpClassName [in, optional]

Type: <b>LPCTSTR</b>

The class name or a class atom created by a previous call to the <a href="/windows/desktop/api/winuser/nf-winuser-registerclassa">RegisterClass</a> or <a href="/windows/desktop/api/winuser/nf-winuser-registerclassexa">RegisterClassEx</a> function. The atom must be in the low-order word of <i>lpClassName</i>; the high-order word must be zero. 

If <i>lpClassName</i> points to a string, it specifies the window class name. The class name can be any name registered with <a href="/windows/desktop/api/winuser/nf-winuser-registerclassa">RegisterClass</a> or <a href="/windows/desktop/api/winuser/nf-winuser-registerclassexa">RegisterClassEx</a>, or any of the predefined control-class names. 

If <i>lpClassName</i> is <b>NULL</b>, it finds any window whose title matches the <i>lpWindowName</i> parameter.

### -param lpWindowName [in, optional]

Type: <b>LPCTSTR</b>

The window name (the window's title). If this parameter is <b>NULL</b>, all window names match.

## -returns

Type: <b>HWND</b>

If the function succeeds, the return value is a handle to the window that has the specified class name and window name.

If the function fails, the return value is <b>NULL</b>. This function does not modify the last error value.

## -remarks

If the <i>lpWindowName</i> parameter is not <b>NULL</b>, <b>FindWindow</b> calls the <a href="/windows/desktop/api/winuser/nf-winuser-getwindowtexta">GetWindowText</a> function to retrieve the window name for comparison. For a description of a potential problem that can arise, see the Remarks for <b>GetWindowText</b>. 


#### Examples

For an example, see <a href="/windows/desktop/inputdev/using-mouse-input">Retrieving the Number of Mouse Wheel Scroll Lines</a>.

<div class="code"></div>




> [!NOTE]
> The winuser.h header defines FindWindow as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-enumwindows">EnumWindows</a>



<a href="/windows/desktop/api/winuser/nf-winuser-findwindowexa">FindWindowEx</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getclassname">GetClassName</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getwindowtexta">GetWindowText</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-registerclassa">RegisterClass</a>



<a href="/windows/desktop/api/winuser/nf-winuser-registerclassexa">RegisterClassEx</a>



<a href="/windows/desktop/winmsg/windows">Windows</a>
