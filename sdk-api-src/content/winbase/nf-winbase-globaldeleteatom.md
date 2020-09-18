---
UID: NF:winbase.GlobalDeleteAtom
title: GlobalDeleteAtom function (winbase.h)
description: Decrements the reference count of a global string atom. If the atom's reference count reaches zero, GlobalDeleteAtom removes the string associated with the atom from the global atom table.
helpviewer_keywords: ["GlobalDeleteAtom","GlobalDeleteAtom function [Data Exchange]","_win32_GlobalDeleteAtom","_win32_globaldeleteatom_cpp","dataxchg.globaldeleteatom","winbase/GlobalDeleteAtom","winui._win32_globaldeleteatom"]
old-location: dataxchg\globaldeleteatom.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\atoms\atomreference\atomfunctions\globaldeleteatom.htm
ms.date: 12/05/2018
ms.keywords: GlobalDeleteAtom, GlobalDeleteAtom function [Data Exchange], _win32_GlobalDeleteAtom, _win32_globaldeleteatom_cpp, dataxchg.globaldeleteatom, winbase/GlobalDeleteAtom, winui._win32_globaldeleteatom
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - GlobalDeleteAtom
 - winbase/GlobalDeleteAtom
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
 - GlobalDeleteAtom
---

# GlobalDeleteAtom function


## -description

Decrements the reference count of a global string atom. If the atom's reference count reaches zero, <b>GlobalDeleteAtom</b> removes the string associated with the atom from the global atom table.

## -parameters

### -param nAtom [in]

Type: <b>ATOM</b>

The atom and character string to be deleted.

## -returns

Type: <b>ATOM</b>

The function always returns (<b>ATOM</b>) 0. 

To determine whether the function has failed, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> with <b>ERROR_SUCCESS</b> before calling <b>GlobalDeleteAtom</b>, then call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. If the last error code is still <b>ERROR_SUCCESS</b>, <b>GlobalDeleteAtom</b> has succeeded.

## -remarks

A string atom's reference count specifies the number of times the string has been added to the atom table. The <a href="/windows/desktop/api/winbase/nf-winbase-globaladdatoma">GlobalAddAtom</a> function increments the reference count of a string that already exists in the global atom table each time it is called. 

Each call to <a href="/windows/desktop/api/winbase/nf-winbase-globaladdatoma">GlobalAddAtom</a> should have a corresponding call to <b>GlobalDeleteAtom</b>. Do not call <b>GlobalDeleteAtom</b> more times than you call <b>GlobalAddAtom</b>, or you may delete the atom while other clients are using it. Applications using Dynamic Data Exchange (DDE) should follow the rules on global atom management to prevent leaks and premature deletion.

<b>GlobalDeleteAtom</b> has no effect on an integer atom (an atom whose value is in the range 0x0001 to 0xBFFF). The function always returns zero for an integer atom.


#### Examples

For an example, see <a href="/windows/desktop/dataxchg/using-dynamic-data-exchange">Initiating a Conversation</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-addatomw">AddAtom</a>



<a href="/windows/desktop/api/winbase/nf-winbase-deleteatom">DeleteAtom</a>



<a href="/windows/desktop/api/winbase/nf-winbase-findatoma">FindAtom</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globaladdatoma">GlobalAddAtom</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globalfindatoma">GlobalFindAtom</a>



<a href="/windows/desktop/api/winbase/nf-winbase-makeintatom">MAKEINTATOM</a>



<b>Reference</b>