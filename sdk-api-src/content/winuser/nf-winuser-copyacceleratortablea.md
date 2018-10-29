---
UID: NF:winuser.CopyAcceleratorTableA
title: CopyAcceleratorTableA function
author: windows-sdk-content
description: Copies the specified accelerator table. This function is used to obtain the accelerator-table data that corresponds to an accelerator-table handle, or to determine the size of the accelerator-table data.
old-location: menurc\copyacceleratortable.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardaccelerators\keyboardacceleratorreference\keyboardacceleratorfunctions\copyacceleratortable.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: CopyAcceleratorTable, CopyAcceleratorTable function [Menus and Other Resources], CopyAcceleratorTableA, CopyAcceleratorTableW, _win32_CopyAcceleratorTable, _win32_copyacceleratortable_cpp, menurc.copyacceleratortable, winui._win32_copyacceleratortable, winuser/CopyAcceleratorTable, winuser/CopyAcceleratorTableA, winuser/CopyAcceleratorTableW
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
req.unicode-ansi: CopyAcceleratorTableW (Unicode) and CopyAcceleratorTableA (ANSI)
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
 - CopyAcceleratorTable
 - CopyAcceleratorTableA
 - CopyAcceleratorTableW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

An array of <a href="https://msdn.microsoft.com/9995bfc3-adc5-4a6d-b834-a96e1ceb6ea0">ACCEL</a> structures that receives the accelerator-table information.


### -param cAccelEntries [in]

Type: <b>int</b>

The number of <a href="https://msdn.microsoft.com/9995bfc3-adc5-4a6d-b834-a96e1ceb6ea0">ACCEL</a> structures to copy to the buffer pointed to by the 
     <i>lpAccelDst</i> parameter.


## -returns



Type: <b>int</b>

If 
      <i>lpAccelDst</i> is <b>NULL</b>, the return value specifies the number of accelerator-table entries in the original table. Otherwise, it specifies the number of accelerator-table entries that were copied.




## -see-also




<a href="https://msdn.microsoft.com/9995bfc3-adc5-4a6d-b834-a96e1ceb6ea0">ACCEL</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/ea8ba5dd-0fa8-4cab-9f48-69fb5cd38a51">CreateAcceleratorTable</a>



<a href="https://msdn.microsoft.com/17fd308f-c1ad-41aa-ae65-72e22a7500f3">DestroyAcceleratorTable</a>



<a href="https://msdn.microsoft.com/cb5e268d-8e38-4682-a736-ecf9bcc34acd">Keyboard Accelerators</a>



<a href="https://msdn.microsoft.com/52ead129-a4fe-413a-a86a-349d4bd816db">LoadAccelerators</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/0d8a970c-68b2-45e6-8702-2490029c1e1d">TranslateAccelerator</a>
 

 

