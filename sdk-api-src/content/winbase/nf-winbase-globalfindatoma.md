---
UID: NF:winbase.GlobalFindAtomA
title: GlobalFindAtomA function (winbase.h)
description: Searches the global atom table for the specified character string and retrieves the global atom associated with that string. (ANSI)
helpviewer_keywords: ["GlobalFindAtomA", "winbase/GlobalFindAtomA"]
old-location: dataxchg\globalfindatom.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\atoms\atomreference\atomfunctions\globalfindatom.htm
ms.date: 12/05/2018
ms.keywords: GlobalFindAtom, GlobalFindAtom function [Data Exchange], GlobalFindAtomA, GlobalFindAtomW, _win32_GlobalFindAtom, _win32_globalfindatom_cpp, dataxchg.globalfindatom, winbase/GlobalFindAtom, winbase/GlobalFindAtomA, winbase/GlobalFindAtomW, winui._win32_globalfindatom
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GlobalFindAtomA
 - winbase/GlobalFindAtomA
dev_langs:
 - c++
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
---

# GlobalFindAtomA function


## -description

Searches the global atom table for the specified character string and retrieves the global atom associated with that string.

## -parameters

### -param lpString [in]

Type: <b>LPCTSTR</b>

The null-terminated character string for which to search. 

Alternatively, you can use an integer atom that has been converted using the <a href="/windows/desktop/api/winbase/nf-winbase-makeintatom">MAKEINTATOM</a> macro. See the Remarks for more information.

## -returns

Type: <b>ATOM</b>

If the function succeeds, the return value is the global atom associated with the given string.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Even though the system preserves the case of a string in an atom table as it was originally entered, the search performed by <b>GlobalFindAtom</b> is not case sensitive. 

If 
				<i>lpString</i> was created by the <a href="/windows/desktop/api/winbase/nf-winbase-makeintatom">MAKEINTATOM</a> macro, the low-order word must be in the range 0x0001 through 0xBFFF. If the low-order word is not in this range, the function fails. 





> [!NOTE]
> The winbase.h header defines GlobalFindAtom as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-addatomw">AddAtom</a>



<a href="/windows/desktop/api/winbase/nf-winbase-deleteatom">DeleteAtom</a>



<a href="/windows/desktop/api/winbase/nf-winbase-findatoma">FindAtom</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getatomnamea">GetAtomName</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globaladdatoma">GlobalAddAtom</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globaldeleteatom">GlobalDeleteAtom</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globalgetatomnamea">GlobalGetAtomName</a>



<b>Reference</b>
