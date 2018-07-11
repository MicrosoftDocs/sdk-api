---
UID: NF:winuser.LoadAcceleratorsW
title: LoadAcceleratorsW function
author: windows-sdk-content
description: Loads the specified accelerator table.
old-location: menurc\loadaccelerators.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardaccelerators\keyboardacceleratorreference\keyboardacceleratorfunctions\loadaccelerators.htm
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: LoadAccelerators, LoadAccelerators function [Menus and Other Resources], LoadAcceleratorsA, LoadAcceleratorsW, _win32_LoadAccelerators, _win32_loadaccelerators_cpp, menurc.loadaccelerators, winui._win32_loadaccelerators, winuser/LoadAccelerators, winuser/LoadAcceleratorsA, winuser/LoadAcceleratorsW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# LoadAcceleratorsW function


## -description


Loads the specified accelerator table.


## -parameters




### -param hInstance [in, optional]

Type: <b>HINSTANCE</b>

A handle to the module whose executable file contains the accelerator table to be loaded.


### -param lpTableName [in]

Type: <b>LPCTSTR</b>

The name of the accelerator table to be loaded. Alternatively, this parameter can specify the resource identifier of an accelerator-table resource in the low-order word and zero in the high-order word. To create this value, use the <a href="https://msdn.microsoft.com/761df981-776f-43ca-9cc9-bb82a49f66e6">MAKEINTRESOURCE</a> macro.


## -returns



Type: <b>HACCEL</b>

If the function succeeds, the return value is a handle to the loaded accelerator table.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If the accelerator table has not yet been loaded, the function loads it from the specified executable file.

Accelerator tables loaded from resources are freed automatically when the application terminates.


#### Examples

For an example, see <a href="using_keyboard_accelerators.htm">Creating Accelerators for Font Attributes</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/9dd87782-aa38-44eb-a35d-3d990cece223">CopyAcceleratorTable</a>



<a href="https://msdn.microsoft.com/ea8ba5dd-0fa8-4cab-9f48-69fb5cd38a51">CreateAcceleratorTable</a>



<a href="https://msdn.microsoft.com/17fd308f-c1ad-41aa-ae65-72e22a7500f3">DestroyAcceleratorTable</a>



<a href="https://msdn.microsoft.com/cb5e268d-8e38-4682-a736-ecf9bcc34acd">Keyboard Accelerators</a>



<a href="https://msdn.microsoft.com/761df981-776f-43ca-9cc9-bb82a49f66e6">MAKEINTRESOURCE</a>



<b>Reference</b>
 

 

