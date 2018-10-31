---
UID: NF:winbase.lstrcatA
title: lstrcatA function
author: windows-sdk-content
description: Appends one string to another.Warning  Do not use.
old-location: menurc\lstrcat.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\lstrcat.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "_win32_lstrcat, _win32_lstrcat_cpp, lstrcat, lstrcat function [Menus and Other Resources], lstrcatA, lstrcatW, menurc.lstrcat, winbase/lstrcat, winbase/lstrcatA, winbase/lstrcatW, winui._win32_lstrcat"
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
req.unicode-ansi: lstrcatW (Unicode) and lstrcatA (ANSI)
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
api_name:
 - lstrcat
 - lstrcatA
 - lstrcatW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lstrcatA function


## -description


Appends one string to another.
<div class="alert"><b>Warning</b>  Do not use. Consider using <a href="https://msdn.microsoft.com/en-us/library/ms647518(v=VS.85).aspx">StringCchCat</a> instead. See Security Considerations. </div><div> </div>

## -parameters




### -param lpString1 [in, out]

Type: <b>LPTSTR</b>

The first null-terminated string. This buffer must be large enough 
				to contain both strings.


### -param lpString2 [in]

Type: <b>LPTSTR</b>

The null-terminated string to be appended to the string 
				specified in the <i>lpString1</i> parameter.


## -returns



Type: <b>LPTSTR</b>

If the function succeeds, the return value is a pointer to the buffer.

If the function fails, the return value is <b>NULL</b> 
                    and <i>lpString1</i> may not be null-terminated.




## -see-also




<b>Conceptual</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms647495(v=VS.85).aspx">StringCbCat</a>



<a href="https://msdn.microsoft.com/en-us/library/ms647496(v=VS.85).aspx">StringCbCatEx</a>



<a href="https://msdn.microsoft.com/en-us/library/ms647497(v=VS.85).aspx">StringCbCatN</a>



<a href="https://msdn.microsoft.com/en-us/library/ms647498(v=VS.85).aspx">StringCbCatNEx</a>



<a href="https://msdn.microsoft.com/en-us/library/ms647518(v=VS.85).aspx">StringCchCat</a>



<a href="https://msdn.microsoft.com/en-us/library/ms647520(v=VS.85).aspx">StringCchCatEx</a>



<a href="https://msdn.microsoft.com/en-us/library/ms647522(v=VS.85).aspx">StringCchCatN</a>



<a href="https://msdn.microsoft.com/en-us/library/ms647524(v=VS.85).aspx">StringCchCatNEx</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646979(v=VS.85).aspx">Strings</a>



<a href="https://msdn.microsoft.com/en-us/library/ms647488(v=VS.85).aspx">lstrcmp</a>



<a href="https://msdn.microsoft.com/en-us/library/ms647489(v=VS.85).aspx">lstrcmpi</a>



<a href="https://msdn.microsoft.com/en-us/library/ms647492(v=VS.85).aspx">lstrlen</a>
 

 

