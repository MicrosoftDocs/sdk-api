---
UID: NF:winbase.GlobalFindAtomW
title: GlobalFindAtomW function
author: windows-sdk-content
description: Searches the global atom table for the specified character string and retrieves the global atom associated with that string.
old-location: dataxchg\globalfindatom.htm
old-project: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\atoms\atomreference\atomfunctions\globalfindatom.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GlobalFindAtom, GlobalFindAtom function [Data Exchange], GlobalFindAtomA, GlobalFindAtomW, _win32_GlobalFindAtom, _win32_globalfindatom_cpp, dataxchg.globalfindatom, winbase/GlobalFindAtom, winbase/GlobalFindAtomA, winbase/GlobalFindAtomW, winui._win32_globalfindatom
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GlobalFindAtomW (Unicode) and GlobalFindAtomA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-atoms-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
api_name:
 - GlobalFindAtom
 - GlobalFindAtomA
 - GlobalFindAtomW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GlobalFindAtomW function


## -description


Searches the global atom table for the specified character string and retrieves the global atom associated with that string. 


## -parameters




### -param lpString [in]

Type: <b>LPCTSTR</b>

The null-terminated character string for which to search. 

Alternatively, you can use an integer atom that has been converted using the <a href="https://msdn.microsoft.com/en-us/library/ms649055(v=VS.85).aspx">MAKEINTATOM</a> macro. See the Remarks for more information. 


## -returns



Type: <b>ATOM</b>

If the function succeeds, the return value is the global atom associated with the given string.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



Even though the system preserves the case of a string in an atom table as it was originally entered, the search performed by <b>GlobalFindAtom</b> is not case sensitive. 

If 
				<i>lpString</i> was created by the <a href="https://msdn.microsoft.com/en-us/library/ms649055(v=VS.85).aspx">MAKEINTATOM</a> macro, the low-order word must be in the range 0x0001 through 0xBFFF. If the low-order word is not in this range, the function fails. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms649056(v=VS.85).aspx">AddAtom</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649057(v=VS.85).aspx">DeleteAtom</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649058(v=VS.85).aspx">FindAtom</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649059(v=VS.85).aspx">GetAtomName</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649060(v=VS.85).aspx">GlobalAddAtom</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649061(v=VS.85).aspx">GlobalDeleteAtom</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649063(v=VS.85).aspx">GlobalGetAtomName</a>



<b>Reference</b>
 

 

