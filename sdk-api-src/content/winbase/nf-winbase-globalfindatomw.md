---
UID: NF:winbase.GlobalFindAtomW
title: GlobalFindAtomW function (winbase.h)
description: Searches the global atom table for the specified character string and retrieves the global atom associated with that string.helpviewer_keywords: ["GlobalFindAtom","GlobalFindAtom function [Data Exchange]","GlobalFindAtomA","GlobalFindAtomW","_win32_GlobalFindAtom","_win32_globalfindatom_cpp","dataxchg.globalfindatom","winbase/GlobalFindAtom","winbase/GlobalFindAtomA","winbase/GlobalFindAtomW","winui._win32_globalfindatom"]
old-location: dataxchg\globalfindatom.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\atoms\atomreference\atomfunctions\globalfindatom.htm
ms.date: 12/05/2018
ms.keywords: GlobalFindAtom, GlobalFindAtom function [Data Exchange], GlobalFindAtomA, GlobalFindAtomW, _win32_GlobalFindAtom, _win32_globalfindatom_cpp, dataxchg.globalfindatom, winbase/GlobalFindAtom, winbase/GlobalFindAtomA, winbase/GlobalFindAtomW, winui._win32_globalfindatom
f1_keywords:
- winbase/GlobalFindAtom
dev_langs:
- c++
req.header: winbase.h
req.include-header: Windows.h
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
- API-MS-Win-Core-atoms-l1-1-0.dll
- kernel32legacy.dll
- API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
api_name:
- GlobalFindAtom
- GlobalFindAtomA
- GlobalFindAtomW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GlobalFindAtomW function


## -description


Searches the global atom table for the specified character string and retrieves the global atom associated with that string. 


## -parameters




### -param lpString [in]

Type: <b>LPCTSTR</b>

The null-terminated character string for which to search. 

Alternatively, you can use an integer atom that has been converted using the <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-makeintatom">MAKEINTATOM</a> macro. See the Remarks for more information. 


## -returns



Type: <b>ATOM</b>

If the function succeeds, the return value is the global atom associated with the given string.

If the function fails, the return value is zero. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. 




## -remarks



Even though the system preserves the case of a string in an atom table as it was originally entered, the search performed by <b>GlobalFindAtom</b> is not case sensitive. 

If 
				<i>lpString</i> was created by the <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-makeintatom">MAKEINTATOM</a> macro, the low-order word must be in the range 0x0001 through 0xBFFF. If the low-order word is not in this range, the function fails. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-addatomw">AddAtom</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-deleteatom">DeleteAtom</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-findatoma">FindAtom</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-getatomnamea">GetAtomName</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-globaladdatoma">GlobalAddAtom</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-globaldeleteatom">GlobalDeleteAtom</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-globalgetatomnamea">GlobalGetAtomName</a>



<b>Reference</b>
 

 

