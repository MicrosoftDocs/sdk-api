---
UID: NF:winbase.FindAtomW
title: FindAtomW function
author: windows-sdk-content
description: Searches the local atom table for the specified character string and retrieves the atom associated with that string.
old-location: dataxchg\findatom.htm
old-project: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\atoms\atomreference\atomfunctions\findatom.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: FindAtom, FindAtom function [Data Exchange], FindAtomA, FindAtomW, _win32_FindAtom, _win32_findatom_cpp, dataxchg.findatom, winbase/FindAtom, winbase/FindAtomA, winbase/FindAtomW, winui._win32_findatom
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
req.unicode-ansi: FindAtomW (Unicode) and FindAtomA (ANSI)
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
 - FindAtom
 - FindAtomA
 - FindAtomW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# FindAtomW function


## -description


Searches the local atom table for the specified character string and retrieves the atom associated with that string. 


## -parameters




### -param lpString [in]

Type: <b>LPCTSTR</b>

The character string for which to search.

Alternatively, you can use an integer atom that has been converted using the <a href="https://msdn.microsoft.com/en-us/library/ms649055(v=VS.85).aspx">MAKEINTATOM</a> macro. See Remarks for more information. 


## -returns



Type: <b>ATOM</b>

If the function succeeds, the return value is the atom associated with the given string. 

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



Even though the system preserves the case of a string in an atom table, the search performed by the <b>FindAtom</b> function is not case sensitive. 

If 
				<i>lpString</i> was created by the <a href="https://msdn.microsoft.com/en-us/library/ms649055(v=VS.85).aspx">MAKEINTATOM</a> macro, the low-order word must be in the range 0x0001 through 0xBFFF. If the low-order word is not in this range, the function fails. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms649056(v=VS.85).aspx">AddAtom</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649057(v=VS.85).aspx">DeleteAtom</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649060(v=VS.85).aspx">GlobalAddAtom</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649061(v=VS.85).aspx">GlobalDeleteAtom</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649062(v=VS.85).aspx">GlobalFindAtom</a>



<b>Reference</b>
 

 

