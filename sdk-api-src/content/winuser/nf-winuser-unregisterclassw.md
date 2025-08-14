---
UID: NF:winuser.UnregisterClassW
title: UnregisterClassW function (winuser.h)
description: Unregisters a window class, freeing the memory required for the class. (Unicode)
helpviewer_keywords: ["UnregisterClass", "UnregisterClass function [Windows and Messages]", "UnregisterClassW", "_win32_UnregisterClass", "_win32_unregisterclass_cpp", "winmsg.unregisterclass", "winui._win32_unregisterclass", "winuser/UnregisterClass", "winuser/UnregisterClassW"]
old-location: winmsg\unregisterclass.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowclasses\windowclassreference\windowclassfunctions\unregisterclass.htm
ms.date: 12/05/2018
ms.keywords: UnregisterClass, UnregisterClass function [Windows and Messages], UnregisterClassA, UnregisterClassW, _win32_UnregisterClass, _win32_unregisterclass_cpp, winmsg.unregisterclass, winui._win32_unregisterclass, winuser/UnregisterClass, winuser/UnregisterClassA, winuser/UnregisterClassW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: UnregisterClassW (Unicode) and UnregisterClassA (ANSI)
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
 - UnregisterClassW
 - winuser/UnregisterClassW
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
 - UnregisterClass
 - UnregisterClassA
 - UnregisterClassW
req.apiset: ext-ms-win-ntuser-windowclass-l1-1-0 (introduced in Windows 8)
---

# UnregisterClassW function


## -description

Unregisters a window class, freeing the memory required for the class.

## -parameters

### -param lpClassName [in]

Type: <b>LPCTSTR</b>

A null-terminated string or a class atom. If <i>lpClassName</i> is a string, it specifies the window class name. This class name must have been registered by a previous call to the <a href="/windows/desktop/api/winuser/nf-winuser-registerclassa">RegisterClass</a> or <a href="/windows/desktop/api/winuser/nf-winuser-registerclassexa">RegisterClassEx</a> function. System classes, such as dialog box controls, cannot be unregistered. If this parameter is an atom, it must be a class atom created by a previous call to the <b>RegisterClass</b> or <b>RegisterClassEx</b> function. The atom must be in the low-order word of <i>lpClassName</i>; the high-order word must be zero.

### -param hInstance [in, optional]

Type: <b>HINSTANCE</b>

A handle to the instance of the module that created the class.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero. 

If the class could not be found or if a window still exists that was created with the class, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Before calling this function, an application must destroy all windows created with the specified class. 

All window classes that an application registers are unregistered when it terminates. 

Class atoms are special atoms returned only by <a href="/windows/desktop/api/winuser/nf-winuser-registerclassa">RegisterClass</a> and <a href="/windows/desktop/api/winuser/nf-winuser-registerclassexa">RegisterClassEx</a>. 

No window classes registered by a DLL are unregistered when the .dll is unloaded. 





> [!NOTE]
> The winuser.h header defines UnregisterClass as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-registerclassa">RegisterClass</a>



<a href="/windows/desktop/api/winuser/nf-winuser-registerclassexa">RegisterClassEx</a>



<a href="/windows/desktop/winmsg/window-classes">Window Classes</a>
