---
UID: NF:winbase.GlobalGetAtomNameW
title: GlobalGetAtomNameW function (winbase.h)
description: Retrieves a copy of the character string associated with the specified global atom. (Unicode)
helpviewer_keywords: ["GlobalGetAtomName", "GlobalGetAtomName function [Data Exchange]", "GlobalGetAtomNameW", "_win32_GlobalGetAtomName", "_win32_globalgetatomname_cpp", "dataxchg.globalgetatomname", "winbase/GlobalGetAtomName", "winbase/GlobalGetAtomNameW", "winui._win32_globalgetatomname"]
old-location: dataxchg\globalgetatomname.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\atoms\atomreference\atomfunctions\globalgetatomname.htm
ms.date: 12/05/2018
ms.keywords: GlobalGetAtomName, GlobalGetAtomName function [Data Exchange], GlobalGetAtomNameA, GlobalGetAtomNameW, _win32_GlobalGetAtomName, _win32_globalgetatomname_cpp, dataxchg.globalgetatomname, winbase/GlobalGetAtomName, winbase/GlobalGetAtomNameA, winbase/GlobalGetAtomNameW, winui._win32_globalgetatomname
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GlobalGetAtomNameW (Unicode) and GlobalGetAtomNameA (ANSI)
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
 - GlobalGetAtomNameW
 - winbase/GlobalGetAtomNameW
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
 - GlobalGetAtomName
 - GlobalGetAtomNameA
 - GlobalGetAtomNameW
---

# GlobalGetAtomNameW function


## -description

Retrieves a copy of the character string associated with the specified global atom.

## -parameters

### -param nAtom [in]

Type: <b>ATOM</b>

The global atom associated with the character string to be retrieved.

### -param lpBuffer [out]

Type: <b>LPTSTR</b>

The buffer for the character string.

### -param nSize [in]

Type: <b>int</b>

The size, in 
					characters, of the buffer.

## -returns

Type: <b>UINT</b>

If the function succeeds, the return value is the length of the string copied to the buffer, in 
						characters, not including the terminating null character.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The string returned for an integer atom (an atom whose value is in the range 0x0001 to 0xBFFF) is a null-terminated string in which the first character is a pound sign (#) and the remaining characters represent the unsigned integer atom value. 

<h3><a id="Security_Considerations"></a><a id="security_considerations"></a><a id="SECURITY_CONSIDERATIONS"></a>Security Considerations</h3>
Using this function incorrectly might compromise the security of your program. Incorrect use of this function includes not correctly specifying the size of the <i>lpBuffer</i> parameter. Also, note that a global atom is accessible by anyone; thus, privacy and the integrity of its contents is not assured.





> [!NOTE]
> The winbase.h header defines GlobalGetAtomName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-addatomw">AddAtom</a>



<a href="/windows/desktop/api/winbase/nf-winbase-deleteatom">DeleteAtom</a>



<a href="/windows/desktop/api/winbase/nf-winbase-findatoma">FindAtom</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globaladdatoma">GlobalAddAtom</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globaldeleteatom">GlobalDeleteAtom</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globalfindatoma">GlobalFindAtom</a>



<a href="/windows/desktop/api/winbase/nf-winbase-makeintatom">MAKEINTATOM</a>



<b>Reference</b>
