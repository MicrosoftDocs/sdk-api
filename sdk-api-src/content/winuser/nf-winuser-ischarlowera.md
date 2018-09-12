---
UID: NF:winuser.IsCharLowerA
title: IsCharLowerA function
author: windows-sdk-content
description: Determines whether a character is lowercase. This determination is based on the semantics of the language selected by the user during setup or through Control Panel.
old-location: menurc\ischarlower.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\ischarlower.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IsCharLower, IsCharLower function [Menus and Other Resources], IsCharLowerA, _win32_IsCharLower, _win32_ischarlower_cpp, menurc.ischarlower, winui._win32_ischarlower, winuser/IsCharLower, winuser/IsCharLowerA
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
req.unicode-ansi: IsCharLowerA (ANSI)
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
 - API-MS-Win-Core-Stringansi-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-user32-l1-1-0.dll
 - API-MS-Win-DownLevel-user32-l1-1-1.dll
api_name:
 - IsCharLower
 - IsCharLowerA
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IsCharLowerA function


## -description


Determines whether a character is lowercase. This determination is based on the semantics of the language selected by the user during setup or through Control Panel. 


## -parameters




### -param ch [in]

Type: <b>TCHAR</b>

The character to be tested.


## -returns



Type: <b>BOOL</b>

If the character is lowercase, the return value is nonzero.

If the character is not lowercase, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms647485(v=VS.85).aspx">IsCharUpper</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646979(v=VS.85).aspx">Strings</a>
 

 

