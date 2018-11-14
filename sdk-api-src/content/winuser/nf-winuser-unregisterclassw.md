---
UID: NF:winuser.UnregisterClassW
title: UnregisterClassW function
author: windows-sdk-content
description: Unregisters a window class, freeing the memory required for the class.
old-location: winmsg\unregisterclass.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowclasses\windowclassreference\windowclassfunctions\unregisterclass.htm
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: UnregisterClass, UnregisterClass function [Windows and Messages], UnregisterClassA, UnregisterClassW, _win32_UnregisterClass, _win32_unregisterclass_cpp, winmsg.unregisterclass, winui._win32_unregisterclass, winuser/UnregisterClass, winuser/UnregisterClassA, winuser/UnregisterClassW
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
req.unicode-ansi: UnregisterClassW (Unicode) and UnregisterClassA (ANSI)
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- UnregisterClassW
: 
---

# UnregisterClassW function


## -description


Unregisters a window class, freeing the memory required for the class. 


## -parameters




### -param lpClassName [in]

Type: <b>LPCTSTR</b>

A null-terminated string or a class atom. If <i>lpClassName</i> is a string, it specifies the window class name. This class name must have been registered by a previous call to the <a href="https://msdn.microsoft.com/en-us/library/ms633586(v=VS.85).aspx">RegisterClass</a> or <a href="https://msdn.microsoft.com/en-us/library/ms633587(v=VS.85).aspx">RegisterClassEx</a> function. System classes, such as dialog box controls, cannot be unregistered. If this parameter is an atom, it must be a class atom created by a previous call to the <b>RegisterClass</b> or <b>RegisterClassEx</b> function. The atom must be in the low-order word of <i>lpClassName</i>; the high-order word must be zero.


### -param hInstance [in, optional]

Type: <b>HINSTANCE</b>

A handle to the instance of the module that created the class. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the function succeeds, the return value is nonzero. 

If the class could not be found or if a window still exists that was created with the class, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



Before calling this function, an application must destroy all windows created with the specified class. 

All window classes that an application registers are unregistered when it terminates. 

Class atoms are special atoms returned only by <a href="https://msdn.microsoft.com/en-us/library/ms633586(v=VS.85).aspx">RegisterClass</a> and <a href="https://msdn.microsoft.com/en-us/library/ms633587(v=VS.85).aspx">RegisterClassEx</a>. 

No window classes registered by a DLL are unregistered when the .dll is unloaded. 




## -see-also




<b>Conceptual</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633586(v=VS.85).aspx">RegisterClass</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633587(v=VS.85).aspx">RegisterClassEx</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632596(v=VS.85).aspx">Window Classes</a>
 

 

