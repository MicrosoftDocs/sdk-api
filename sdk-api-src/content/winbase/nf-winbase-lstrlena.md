---
UID: NF:winbase.lstrlenA
title: lstrlenA function
author: windows-sdk-content
description: Determines the length of the specified string (not including the terminating null character).
old-location: menurc\lstrlen.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\lstrlen.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "_win32_lstrlen, _win32_lstrlen_cpp, lstrlen, lstrlen function [Menus and Other Resources], lstrlenA, lstrlenW, menurc.lstrlen, winbase/lstrlen, winbase/lstrlenA, winbase/lstrlenW, winui._win32_lstrlen"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lstrlenW (Unicode) and lstrlenA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-String-Obsolete-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-String-Obsolete-l1-1-1.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-misc-l1-1-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
api_name:
 - lstrlen
 - lstrlenA
 - lstrlenW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lstrlenA function


## -description


Determines the length of the specified string (not including the terminating null character).


## -parameters




### -param lpString [in]

Type: <b>LPCTSTR</b>

The null-terminated string to be checked.


## -returns



Type: <b>int</b>

The function returns the length of the string, in characters. If <i>lpString</i> is <b>NULL</b>, the function returns 0.




## -see-also




<b>Conceptual</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms647509(v=VS.85).aspx">StringCbLength</a>



<a href="https://msdn.microsoft.com/en-us/library/ms647539(v=VS.85).aspx">StringCchLength</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646979(v=VS.85).aspx">Strings</a>



<a href="https://msdn.microsoft.com/en-us/library/ms647487(v=VS.85).aspx">lstrcat</a>



<a href="https://msdn.microsoft.com/en-us/library/ms647488(v=VS.85).aspx">lstrcmp</a>



<a href="https://msdn.microsoft.com/en-us/library/ms647489(v=VS.85).aspx">lstrcmpi</a>



<a href="https://msdn.microsoft.com/en-us/library/ms647490(v=VS.85).aspx">lstrcpy</a>
 

 

