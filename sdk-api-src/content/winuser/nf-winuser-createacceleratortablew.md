---
UID: NF:winuser.CreateAcceleratorTableW
title: CreateAcceleratorTableW function (winuser.h)
author: windows-sdk-content
description: Creates an accelerator table.
old-location: menurc\createacceleratortable.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardaccelerators\keyboardacceleratorreference\keyboardacceleratorfunctions\createacceleratortable.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateAcceleratorTable, CreateAcceleratorTable function [Menus and Other Resources], CreateAcceleratorTableA, CreateAcceleratorTableW, _win32_CreateAcceleratorTable, _win32_createacceleratortable_cpp, menurc.createacceleratortable, winui._win32_createacceleratortable, winuser/CreateAcceleratorTable, winuser/CreateAcceleratorTableA, winuser/CreateAcceleratorTableW
ms.topic: function
f1_keywords: 
 - "winuser/CreateAcceleratorTable"
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateAcceleratorTableW (Unicode) and CreateAcceleratorTableA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-Keyboard-l1-1-2.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-0.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-1.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-3-0.dll
api_name:
 - CreateAcceleratorTable
 - CreateAcceleratorTableA
 - CreateAcceleratorTableW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CreateAcceleratorTableW function


## -description


Creates an accelerator table.


## -parameters




### -param paccel [in]

Type: <b>LPACCEL</b>

An array of <a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-accel">ACCEL</a> structures that describes the accelerator table.


### -param cAccel [in]

Type: <b>int</b>

The number of <a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-accel">ACCEL</a> structures in the array. This must be within the range 1 to 32767 or the function will fail.


## -returns



Type: <b>HACCEL</b>

If the function succeeds, the return value is the handle to the created accelerator table; otherwise, it is <b>NULL</b>. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



Before an application closes, it can use the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-destroyacceleratortable">DestroyAcceleratorTable</a> function to destroy any accelerator tables that it created by using the <b>CreateAcceleratorTable</b> function.


#### Examples

For an example, see <a href="https://docs.microsoft.com/windows/desktop/menurc/using-keyboard-accelerators">Creating User Editable Accelerators</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-accel">ACCEL</a>



<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-copyacceleratortablea">CopyAcceleratorTable</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-destroyacceleratortable">DestroyAcceleratorTable</a>



<a href="https://docs.microsoft.com/windows/desktop/menurc/keyboard-accelerators">Keyboard Accelerators</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-loadacceleratorsa">LoadAccelerators</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-translateacceleratora">TranslateAccelerator</a>
 

 

