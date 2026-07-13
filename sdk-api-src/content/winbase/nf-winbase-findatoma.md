---
UID: NF:winbase.FindAtomA
title: FindAtomA function (winbase.h)
description: Searches the local atom table for the specified character string and retrieves the atom associated with that string. (ANSI)
helpviewer_keywords: ["FindAtomA", "winbase/FindAtomA"]
old-location: dataxchg\findatom.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\atoms\atomreference\atomfunctions\findatom.htm
ms.date: 12/05/2018
ms.keywords: FindAtom, FindAtom function [Data Exchange], FindAtomA, FindAtomW, _win32_FindAtom, _win32_findatom_cpp, dataxchg.findatom, winbase/FindAtom, winbase/FindAtomA, winbase/FindAtomW, winui._win32_findatom
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FindAtomA
 - winbase/FindAtomA
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
 - FindAtom
 - FindAtomA
 - FindAtomW
---

# FindAtomA function


## -description

Searches the local atom table for the specified character string and retrieves the atom associated with that string.

## -parameters

### -param lpString [in]

Type: <b>LPCTSTR</b>

The character string for which to search.

Alternatively, you can use an integer atom that has been converted using the <a href="/windows/desktop/api/winbase/nf-winbase-makeintatom">MAKEINTATOM</a> macro. See Remarks for more information.

## -returns

Type: <b>ATOM</b>

If the function succeeds, the return value is the atom associated with the given string. 

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Even though the system preserves the case of a string in an atom table, the search performed by the <b>FindAtom</b> function is not case sensitive. 

If 
				<i>lpString</i> was created by the <a href="/windows/desktop/api/winbase/nf-winbase-makeintatom">MAKEINTATOM</a> macro, the low-order word must be in the range 0x0001 through 0xBFFF. If the low-order word is not in this range, the function fails. 





> [!NOTE]
> The winbase.h header defines FindAtom as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-addatomw">AddAtom</a>



<a href="/windows/desktop/api/winbase/nf-winbase-deleteatom">DeleteAtom</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globaladdatoma">GlobalAddAtom</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globaldeleteatom">GlobalDeleteAtom</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globalfindatoma">GlobalFindAtom</a>



<b>Reference</b>
