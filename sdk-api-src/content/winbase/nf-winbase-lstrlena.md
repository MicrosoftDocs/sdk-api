---
UID: NF:winbase.lstrlenA
title: lstrlenA function
author: windows-sdk-content
description: Determines the length of the specified string (not including the terminating null character).
old-location: menurc\lstrlen.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\lstrlen.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: "_win32_lstrlen, _win32_lstrlen_cpp, lstrlen, lstrlen function [Menus and Other Resources], lstrlenA, lstrlenW, menurc.lstrlen, winbase/lstrlen, winbase/lstrlenA, winbase/lstrlenW, winui._win32_lstrlen"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-String-Obsolete-l1-1-0.dll
-	kernel32legacy.dll
-	API-MS-Win-Core-String-Obsolete-l1-1-1.dll
-	API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
-	API-MS-Win-Core-misc-l1-1-0.dll
-	KernelBase.dll
-	MinKernelBase.dll
api_name:
-	lstrlen
-	lstrlenA
-	lstrlenW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
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



<a href="https://msdn.microsoft.com/a1aa834c-53e7-4321-9db4-86f32ef31dc4">StringCbLength</a>



<a href="https://msdn.microsoft.com/4b29469a-e9a8-4309-9d19-db74a8bd6038">StringCchLength</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563884">Strings</a>



<a href="https://msdn.microsoft.com/346f6c95-6ebe-4e73-8f29-2778cc813e36">lstrcat</a>



<a href="https://msdn.microsoft.com/e7b6ac43-ef24-4121-bb4e-a01232b034ad">lstrcmp</a>



<a href="https://msdn.microsoft.com/7edd4896-04d3-4b71-9ce6-d64149d683e0">lstrcmpi</a>



<a href="https://msdn.microsoft.com/3960fe0e-954d-4463-bc81-e1682e468278">lstrcpy</a>
 

 

