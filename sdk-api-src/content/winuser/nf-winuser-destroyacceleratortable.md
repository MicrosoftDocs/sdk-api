---
UID: NF:winuser.DestroyAcceleratorTable
title: DestroyAcceleratorTable function (winuser.h)
description: Destroys an accelerator table.
helpviewer_keywords: ["DestroyAcceleratorTable","DestroyAcceleratorTable function [Menus and Other Resources]","_win32_DestroyAcceleratorTable","_win32_destroyacceleratortable_cpp","menurc.destroyacceleratortable","winui._win32_destroyacceleratortable","winuser/DestroyAcceleratorTable"]
old-location: menurc\destroyacceleratortable.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardaccelerators\keyboardacceleratorreference\keyboardacceleratorfunctions\destroyacceleratortable.htm
ms.date: 12/05/2018
ms.keywords: DestroyAcceleratorTable, DestroyAcceleratorTable function [Menus and Other Resources], _win32_DestroyAcceleratorTable, _win32_destroyacceleratortable_cpp, menurc.destroyacceleratortable, winui._win32_destroyacceleratortable, winuser/DestroyAcceleratorTable
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
 - DestroyAcceleratorTable
 - winuser/DestroyAcceleratorTable
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
 - ext-ms-win-ntuser-keyboard-l1-1-2.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-0.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-1.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-3-0.dll
api_name:
 - DestroyAcceleratorTable
---

# DestroyAcceleratorTable function


## -description

Destroys an accelerator table.

## -parameters

### -param hAccel [in]

Type: <b>HACCEL</b>

A handle to the accelerator table to be destroyed. This handle must have been created by a call to the <a href="/windows/desktop/api/winuser/nf-winuser-createacceleratortablea">CreateAcceleratorTable</a> or <a href="/windows/desktop/api/winuser/nf-winuser-loadacceleratorsa">LoadAccelerators</a> function.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero. However, if the table has been loaded more than one call to <a href="/windows/desktop/api/winuser/nf-winuser-loadacceleratorsa">LoadAccelerators</a>, the function will return a nonzero value only when <b>DestroyAcceleratorTable</b> has been called an equal number of times.

If the function fails, the return value is zero.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-copyacceleratortablea">CopyAcceleratorTable</a>



<a href="/windows/desktop/api/winuser/nf-winuser-createacceleratortablea">CreateAcceleratorTable</a>



<a href="/windows/desktop/menurc/keyboard-accelerators">Keyboard Accelerators</a>



<a href="/windows/desktop/api/winuser/nf-winuser-loadacceleratorsa">LoadAccelerators</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-translateacceleratora">TranslateAccelerator</a>