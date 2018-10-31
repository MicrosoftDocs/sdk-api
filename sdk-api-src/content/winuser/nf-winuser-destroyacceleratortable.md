---
UID: NF:winuser.DestroyAcceleratorTable
title: DestroyAcceleratorTable function
author: windows-sdk-content
description: Destroys an accelerator table.
old-location: menurc\destroyacceleratortable.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardaccelerators\keyboardacceleratorreference\keyboardacceleratorfunctions\destroyacceleratortable.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: DestroyAcceleratorTable, DestroyAcceleratorTable function [Menus and Other Resources], _win32_DestroyAcceleratorTable, _win32_destroyacceleratortable_cpp, menurc.destroyacceleratortable, winui._win32_destroyacceleratortable, winuser/DestroyAcceleratorTable
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - ext-ms-win-ntuser-keyboard-l1-1-2.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-0.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-1.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-3-0.dll
api_name:
 - DestroyAcceleratorTable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DestroyAcceleratorTable function


## -description


Destroys an accelerator table.


## -parameters




### -param hAccel [in]

Type: <b>HACCEL</b>

A handle to the accelerator table to be destroyed. This handle must have been created by a call to the <a href="https://msdn.microsoft.com/ea8ba5dd-0fa8-4cab-9f48-69fb5cd38a51">CreateAcceleratorTable</a> or <a href="https://msdn.microsoft.com/52ead129-a4fe-413a-a86a-349d4bd816db">LoadAccelerators</a> function.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero. However, if the table has been loaded more than one call to <a href="https://msdn.microsoft.com/52ead129-a4fe-413a-a86a-349d4bd816db">LoadAccelerators</a>, the function will return a nonzero value only when <b>DestroyAcceleratorTable</b> has been called an equal number of times.

If the function fails, the return value is zero.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/9dd87782-aa38-44eb-a35d-3d990cece223">CopyAcceleratorTable</a>



<a href="https://msdn.microsoft.com/ea8ba5dd-0fa8-4cab-9f48-69fb5cd38a51">CreateAcceleratorTable</a>



<a href="https://msdn.microsoft.com/cb5e268d-8e38-4682-a736-ecf9bcc34acd">Keyboard Accelerators</a>



<a href="https://msdn.microsoft.com/52ead129-a4fe-413a-a86a-349d4bd816db">LoadAccelerators</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/0d8a970c-68b2-45e6-8702-2490029c1e1d">TranslateAccelerator</a>
 

 

