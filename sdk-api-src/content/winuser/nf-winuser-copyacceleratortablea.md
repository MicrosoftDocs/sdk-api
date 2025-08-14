---
UID: NF:winuser.CopyAcceleratorTableA
title: CopyAcceleratorTableA function (winuser.h)
description: Copies the specified accelerator table. This function is used to obtain the accelerator-table data that corresponds to an accelerator-table handle, or to determine the size of the accelerator-table data. (ANSI)
helpviewer_keywords: ["CopyAcceleratorTableA", "winuser/CopyAcceleratorTableA"]
old-location: menurc\copyacceleratortable.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardaccelerators\keyboardacceleratorreference\keyboardacceleratorfunctions\copyacceleratortable.htm
ms.date: 12/05/2018
ms.keywords: CopyAcceleratorTable, CopyAcceleratorTable function [Menus and Other Resources], CopyAcceleratorTableA, CopyAcceleratorTableW, _win32_CopyAcceleratorTable, _win32_copyacceleratortable_cpp, menurc.copyacceleratortable, winui._win32_copyacceleratortable, winuser/CopyAcceleratorTable, winuser/CopyAcceleratorTableA, winuser/CopyAcceleratorTableW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CopyAcceleratorTableW (Unicode) and CopyAcceleratorTableA (ANSI)
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
 - CopyAcceleratorTableA
 - winuser/CopyAcceleratorTableA
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
 - Ext-MS-Win-NTUser-Keyboard-l1-1-2.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-0.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-1.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-3-0.dll
api_name:
 - CopyAcceleratorTable
 - CopyAcceleratorTableA
 - CopyAcceleratorTableW
---

# CopyAcceleratorTableA function


## -description

Copies the specified accelerator table. This function is used to obtain the accelerator-table data that corresponds to an accelerator-table handle, or to determine the size of the accelerator-table data.

## -parameters

### -param hAccelSrc [in]

Type: <b>HACCEL</b>

A handle to the accelerator table to copy.

### -param lpAccelDst [out, optional]

Type: <b>LPACCEL</b>

An array of <a href="/windows/desktop/api/winuser/ns-winuser-accel">ACCEL</a> structures that receives the accelerator-table information.

### -param cAccelEntries [in]

Type: <b>int</b>

The number of <a href="/windows/desktop/api/winuser/ns-winuser-accel">ACCEL</a> structures to copy to the buffer pointed to by the 
     <i>lpAccelDst</i> parameter.

## -returns

Type: <b>int</b>

If 
      <i>lpAccelDst</i> is <b>NULL</b>, the return value specifies the number of accelerator-table entries in the original table. Otherwise, it specifies the number of accelerator-table entries that were copied.

## -see-also

<a href="/windows/desktop/api/winuser/ns-winuser-accel">ACCEL</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-createacceleratortablea">CreateAcceleratorTable</a>



<a href="/windows/desktop/api/winuser/nf-winuser-destroyacceleratortable">DestroyAcceleratorTable</a>



<a href="/windows/desktop/menurc/keyboard-accelerators">Keyboard Accelerators</a>



<a href="/windows/desktop/api/winuser/nf-winuser-loadacceleratorsa">LoadAccelerators</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-translateacceleratora">TranslateAccelerator</a>

## -remarks

> [!NOTE]
> The winuser.h header defines CopyAcceleratorTable as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
