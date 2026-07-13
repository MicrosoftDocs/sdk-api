---
UID: NF:winuser.GetClassInfoExA
title: GetClassInfoExA function (winuser.h)
description: Retrieves information about a window class, including a handle to the small icon associated with the window class. The GetClassInfo function does not retrieve a handle to the small icon. (ANSI)
helpviewer_keywords: ["GetClassInfoExA", "winuser/GetClassInfoExA"]
old-location: winmsg\getclassinfoex.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowclasses\windowclassreference\windowclassfunctions\getclassinfoex.htm
ms.date: 12/05/2018
ms.keywords: GetClassInfoEx, GetClassInfoEx function [Windows and Messages], GetClassInfoExA, GetClassInfoExW, _win32_GetClassInfoEx, _win32_getclassinfoex_cpp, winmsg.getclassinfoex, winui._win32_getclassinfoex, winuser/GetClassInfoEx, winuser/GetClassInfoExA, winuser/GetClassInfoExW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetClassInfoExW (Unicode) and GetClassInfoExA (ANSI)
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
 - GetClassInfoExA
 - winuser/GetClassInfoExA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
 - GetClassInfoEx
 - GetClassInfoExA
 - GetClassInfoExW
req.apiset: ext-ms-win-ntuser-windowclass-l1-1-0 (introduced in Windows 8)
---

# GetClassInfoExA function


## -description

Retrieves information about a window class, including a handle to the small icon associated with the window class. The <a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoa">GetClassInfo</a> function does not retrieve a handle to the small icon.

## -parameters

### -param hInstance [in, optional]

Type: <b>HINSTANCE</b>

A handle to the instance of the application that created the class. To retrieve information about classes defined by the system (such as buttons or list boxes), set this parameter to <b>NULL</b>.

### -param lpszClass [in]

Type: <b>LPCTSTR</b>

The class name. The name must be that of a preregistered class or a class registered by a previous call to the <a href="/windows/desktop/api/winuser/nf-winuser-registerclassa">RegisterClass</a> or <a href="/windows/desktop/api/winuser/nf-winuser-registerclassexa">RegisterClassEx</a> function. Alternatively, this parameter can be a class atom created by a previous call to <b>RegisterClass</b> or <b>RegisterClassEx</b>. The atom must be in the low-order word of 
					<i>lpszClass</i>; the high-order word must be zero.

### -param lpwcx [out]

Type: <b>LPWNDCLASSEX</b>

A pointer to a <a href="/windows/desktop/api/winuser/ns-winuser-wndclassexa">WNDCLASSEX</a> structure that receives the information about the class.

## -returns

Type: <b>BOOL</b>

If the function finds a matching class and successfully copies the data, the return value is nonzero.

If the function does not find a matching class and successfully copy the data, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Class atoms are created using the <a href="/windows/desktop/api/winuser/nf-winuser-registerclassa">RegisterClass</a> or <a href="/windows/desktop/api/winuser/nf-winuser-registerclassexa">RegisterClassEx</a> function, not the 
				<a href="/windows/desktop/api/winbase/nf-winbase-globaladdatoma">GlobalAddAtom</a> function. 





> [!NOTE]
> The winuser.h header defines GetClassInfoEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getclasslonga">GetClassLong</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getclassname">GetClassName</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-registerclassa">RegisterClass</a>



<a href="/windows/desktop/api/winuser/nf-winuser-registerclassexa">RegisterClassEx</a>



<a href="/windows/desktop/winmsg/window-classes">Window Classes</a>
