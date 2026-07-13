---
UID: NF:winbase.AddAtomW
title: AddAtomW function (winbase.h)
description: Adds a character string to the local atom table and returns a unique value (an atom) identifying the string. (Unicode)
helpviewer_keywords: ["AddAtom", "AddAtom function [Data Exchange]", "AddAtomW", "_win32_AddAtom", "_win32_addatom_cpp", "dataxchg.addatom", "winbase/AddAtom", "winbase/AddAtomW", "winui._win32_addatom"]
old-location: dataxchg\addatom.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\atoms\atomreference\atomfunctions\addatom.htm
ms.date: 12/05/2018
ms.keywords: AddAtom, AddAtom function [Data Exchange], AddAtomA, AddAtomW, _win32_AddAtom, _win32_addatom_cpp, dataxchg.addatom, winbase/AddAtom, winbase/AddAtomA, winbase/AddAtomW, winui._win32_addatom
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: AddAtomW (Unicode) and AddAtomA (ANSI)
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
 - AddAtomW
 - winbase/AddAtomW
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
 - AddAtom
 - AddAtomA
 - AddAtomW
---

# AddAtomW function


## -description

Adds a character string to the local atom table and returns a unique value (an atom) identifying the string.

## -parameters

### -param lpString [in]

Type: <b>LPCTSTR</b>

The null-terminated string to be added. The string can have a maximum size of 255 bytes. Strings differing only in case are considered identical. The case of the first string added is preserved and returned by the <a href="/windows/desktop/api/winbase/nf-winbase-getatomnamea">GetAtomName</a> function. 

Alternatively, you can use an integer atom that has been converted using the <a href="/windows/desktop/api/winbase/nf-winbase-makeintatom">MAKEINTATOM</a> macro. See the Remarks for more information.

## -returns

Type: <b>ATOM</b>

If the function succeeds, the return value is the newly created atom.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>AddAtom</b> function stores no more than one copy of a given string in the atom table. If the string is already in the table, the function returns the existing atom and, in the case of a string atom, increments the string's reference count. 

If 
				<i>lpString</i> has the form "#1234", <b>AddAtom</b> returns an integer atom whose value is the 16-bit representation of the decimal number specified in the string (0x04D2, in this example). If the decimal value specified is 0x0000 or is greater than or equal to 0xC000, the return value is zero, indicating an error. If 
				<i>lpString</i> was created by the <a href="/windows/desktop/api/winbase/nf-winbase-makeintatom">MAKEINTATOM</a> macro, the low-order word must be in the range 0x0001 through 0xBFFF. If the low-order word is not in this range, the function fails. 

If 
				<i>lpString</i> has any other form, <b>AddAtom</b> returns a string atom. 





> [!NOTE]
> The winbase.h header defines AddAtom as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-deleteatom">DeleteAtom</a>



<a href="/windows/desktop/api/winbase/nf-winbase-findatoma">FindAtom</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getatomnamea">GetAtomName</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globaladdatoma">GlobalAddAtom</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globaldeleteatom">GlobalDeleteAtom</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globalfindatoma">GlobalFindAtom</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globalgetatomnamea">GlobalGetAtomName</a>



<a href="/windows/desktop/api/winbase/nf-winbase-makeintatom">MAKEINTATOM</a>



<b>Reference</b>
