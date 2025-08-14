---
UID: NF:winuser.RegisterClassExW
title: RegisterClassExW function (winuser.h)
description: Registers a window class for subsequent use in calls to the CreateWindow or CreateWindowEx function. (RegisterClassExW)
helpviewer_keywords: ["RegisterClassEx", "RegisterClassEx function [Windows and Messages]", "RegisterClassExW", "_win32_RegisterClassEx", "_win32_registerclassex_cpp", "winmsg.registerclassex", "winui._win32_registerclassex", "winuser/RegisterClassEx", "winuser/RegisterClassExW"]
old-location: winmsg\registerclassex.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowclasses\windowclassreference\windowclassfunctions\registerclassex.htm
ms.date: 12/05/2018
ms.keywords: RegisterClassEx, RegisterClassEx function [Windows and Messages], RegisterClassExA, RegisterClassExW, _win32_RegisterClassEx, _win32_registerclassex_cpp, winmsg.registerclassex, winui._win32_registerclassex, winuser/RegisterClassEx, winuser/RegisterClassExA, winuser/RegisterClassExW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegisterClassExW (Unicode) and RegisterClassExA (ANSI)
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
 - RegisterClassExW
 - winuser/RegisterClassExW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-window-l1-1-0.dll
 - ext-ms-win-rtcore-ntuser-window-ext-l1-1-1.dll
 - User32.dll
 - API-MS-Win-NTUser-IE-Window-l1-1-0.dll
 - ie_shims.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-Windowclass-l1-1-0.dll
 - Ext-MS-Win-NTUser-Windowclass-l1-1-1.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - ext-ms-win-ntuser-windowclass-l1-1-2.dll
api_name:
 - RegisterClassEx
 - RegisterClassExA
 - RegisterClassExW
req.apiset: ext-ms-win-ntuser-windowclass-l1-1-0 (introduced in Windows 8)
---

# RegisterClassExW function


## -description

Registers a window class for subsequent use in calls to the <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa">CreateWindow</a> or <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa">CreateWindowEx</a> function.

## -parameters

### -param unnamedParam1 [in]

Type: <b>const WNDCLASSEX*</b>

A pointer to a <a href="/windows/desktop/api/winuser/ns-winuser-wndclassexa">WNDCLASSEX</a> structure. You must fill the structure with the appropriate class attributes before passing it to the function.

## -returns

Type: <b>ATOM</b>

If the function succeeds, the return value is a class atom that uniquely identifies the class being registered. This atom can only be used by the <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa">CreateWindow</a>, <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa">CreateWindowEx</a>, <a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoa">GetClassInfo</a>, <a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoexa">GetClassInfoEx</a>, <a href="/windows/desktop/api/winuser/nf-winuser-findwindowa">FindWindow</a>, <a href="/windows/desktop/api/winuser/nf-winuser-findwindowexa">FindWindowEx</a>, and <a href="/windows/desktop/api/winuser/nf-winuser-unregisterclassa">UnregisterClass</a> functions and the <b>IActiveIMMap::FilterClientWindows</b> method. 

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If you register the window class by using 
				<b>RegisterClassExA</b>, the application tells the system that the windows of the created class expect messages with text or character parameters to use the ANSI character set; if you register it by using 
				<b>RegisterClassExW</b>, the application requests that the system pass text parameters of messages as Unicode. The <a href="/windows/desktop/api/winuser/nf-winuser-iswindowunicode">IsWindowUnicode</a> function enables applications to query the nature of each window. For more information on ANSI and Unicode functions, see <a href="/windows/desktop/Intl/conventions-for-function-prototypes">Conventions for Function Prototypes</a>.

All window classes that an application registers are unregistered when it terminates. 

No window classes registered by a DLL are unregistered when the DLL is unloaded. A DLL must explicitly unregister its classes when it is unloaded. 



#### Examples

For an example, see <a href="/windows/desktop/winmsg/using-window-classes">Using Window Classes</a>.

<div class="code"></div>




> [!NOTE]
> The winuser.h header defines RegisterClassEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-createwindowa">CreateWindow</a>



<a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa">CreateWindowEx</a>



<a href="/windows/desktop/api/winuser/nf-winuser-findwindowa">FindWindow</a>



<a href="/windows/desktop/api/winuser/nf-winuser-findwindowexa">FindWindowEx</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoa">GetClassInfo</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoexa">GetClassInfoEx</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getclassname">GetClassName</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-registerclassa">RegisterClass</a>



<a href="/windows/desktop/api/winuser/nf-winuser-unregisterclassa">UnregisterClass</a>



<a href="/windows/desktop/api/winuser/ns-winuser-wndclassexa">WNDCLASSEX</a>



<a href="/windows/desktop/winmsg/window-classes">Window Classes</a>



<a href="/windows/win32/api/winuser/nc-winuser-wndproc">WindowProc</a>
