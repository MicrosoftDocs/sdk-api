---
UID: NF:winuser.LoadAcceleratorsA
title: LoadAcceleratorsA function (winuser.h)
description: Loads the specified accelerator table. (ANSI)
helpviewer_keywords: ["LoadAcceleratorsA", "winuser/LoadAcceleratorsA"]
old-location: menurc\loadaccelerators.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardaccelerators\keyboardacceleratorreference\keyboardacceleratorfunctions\loadaccelerators.htm
ms.date: 12/05/2018
ms.keywords: LoadAccelerators, LoadAccelerators function [Menus and Other Resources], LoadAcceleratorsA, LoadAcceleratorsW, _win32_LoadAccelerators, _win32_loadaccelerators_cpp, menurc.loadaccelerators, winui._win32_loadaccelerators, winuser/LoadAccelerators, winuser/LoadAcceleratorsA, winuser/LoadAcceleratorsW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LoadAcceleratorsW (Unicode) and LoadAcceleratorsA (ANSI)
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
 - LoadAcceleratorsA
 - winuser/LoadAcceleratorsA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-keyboard-ansi-l1-1-0.dll
 - User32.dll
 - Ext-MS-Win-NTUser-Keyboard-l1-1-0.dll
 - Ext-MS-Win-NTUser-Keyboard-l1-1-1.dll
 - api-ms-win-ntuser-ie-keyboard-l1-1-0.dll
 - ie_stubs.dll
 - ext-ms-win-ntuser-keyboard-l1-1-2.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-0.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-1.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-3-0.dll
api_name:
 - LoadAccelerators
 - LoadAcceleratorsA
 - LoadAcceleratorsW
---

# LoadAcceleratorsA function


## -description

Loads the specified accelerator table.

## -parameters

### -param hInstance [in, optional]

Type: <b>HINSTANCE</b>

A handle to the module whose executable file contains the accelerator table to be loaded.

### -param lpTableName [in]

Type: <b>LPCTSTR</b>

The name of the accelerator table to be loaded. Alternatively, this parameter can specify the resource identifier of an accelerator-table resource in the low-order word and zero in the high-order word. To create this value, use the <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a> macro.

## -returns

Type: <b>HACCEL</b>

If the function succeeds, the return value is a handle to the loaded accelerator table.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the accelerator table has not yet been loaded, the function loads it from the specified executable file.

Accelerator tables loaded from resources are freed automatically when the application terminates.


#### Examples

For an example, see <a href="/windows/desktop/menurc/using-keyboard-accelerators">Creating Accelerators for Font Attributes</a>.

<div class="code"></div>




> [!NOTE]
> The winuser.h header defines LoadAccelerators as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-copyacceleratortablea">CopyAcceleratorTable</a>



<a href="/windows/desktop/api/winuser/nf-winuser-createacceleratortablea">CreateAcceleratorTable</a>



<a href="/windows/desktop/api/winuser/nf-winuser-destroyacceleratortable">DestroyAcceleratorTable</a>



<a href="/windows/desktop/menurc/keyboard-accelerators">Keyboard Accelerators</a>



<a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a>



<b>Reference</b>
