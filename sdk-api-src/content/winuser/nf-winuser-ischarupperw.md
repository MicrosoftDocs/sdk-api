---
UID: NF:winuser.IsCharUpperW
title: IsCharUpperW function (winuser.h)
author: windows-sdk-content
description: Determines whether a character is uppercase. This determination is based on the semantics of the language selected by the user during setup or through Control Panel.
old-location: menurc\ischarupper.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\ischarupper.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IsCharUpper, IsCharUpper function [Menus and Other Resources], IsCharUpperA, IsCharUpperW, _win32_IsCharUpper, _win32_ischarupper_cpp, menurc.ischarupper, winui._win32_ischarupper, winuser/IsCharUpper, winuser/IsCharUpperA, winuser/IsCharUpperW
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: IsCharUpperW (Unicode) and IsCharUpperA (ANSI)
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
 - API-MS-Win-Core-String-l2-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-String-l2-1-1.dll
 - API-MS-Win-Core-Stringansi-l1-1-0.dll
 - API-MS-Win-DownLevel-user32-l1-1-0.dll
 - API-MS-Win-DownLevel-user32-l1-1-1.dll
api_name:
 - IsCharUpper
 - IsCharUpperA
 - IsCharUpperW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IsCharUpperW function


## -description


Determines whether a character is uppercase. This determination is based on the semantics of the language selected by the user during setup or through Control Panel. 


## -parameters




### -param ch [in]

Type: <b>TCHAR</b>

The character to be tested.


## -returns



Type: <b>BOOL</b>

If the character is uppercase, the return value is nonzero.

If the character is not uppercase, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms647484(v=VS.85).aspx">IsCharLower</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646979(v=VS.85).aspx">Strings</a>
 

 

