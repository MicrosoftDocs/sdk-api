---
UID: NF:winbase.InitAtomTable
title: InitAtomTable function (winbase.h)
description: Initializes the local atom table and sets the number of hash buckets to the specified size.
helpviewer_keywords: ["InitAtomTable","InitAtomTable function [Data Exchange]","_win32_InitAtomTable","_win32_initatomtable_cpp","dataxchg.initatomtable","winbase/InitAtomTable","winui._win32_initatomtable"]
old-location: dataxchg\initatomtable.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\atoms\atomreference\atomfunctions\initatomtable.htm
ms.date: 12/05/2018
ms.keywords: InitAtomTable, InitAtomTable function [Data Exchange], _win32_InitAtomTable, _win32_initatomtable_cpp, dataxchg.initatomtable, winbase/InitAtomTable, winui._win32_initatomtable
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
 - InitAtomTable
 - winbase/InitAtomTable
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
 - InitAtomTable
---

# InitAtomTable function


## -description

Initializes the local atom table and sets the number of hash buckets to the specified size.

## -parameters

### -param nSize [in]

Type: <b>DWORD</b>

The number of hash buckets to use for the atom table. If this parameter is zero, the default number of hash buckets are created.

To achieve better performance, specify a prime number in 
					<i>nSize</i>.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

An application need not use this function to use a local atom table. The default number of hash buckets used is 37. If an application does use <b>InitAtomTable</b>, however, it should call the function before any other atom-management function. 

If an application uses a large number of local atoms, it can reduce the time required to add an atom to the local atom table or to find an atom in the table by increasing the size of the table. However, this increases the amount of memory required to maintain the table. 

The number of buckets in the global atom table cannot be changed. If the atom table has already been initialized, either explicitly by a prior call to <b>InitAtomTable</b>, or implicitly by the use of any atom-management function, <b>InitAtomTable</b> returns success without changing the number of hash buckets.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-addatomw">AddAtom</a>



<a href="/windows/desktop/api/winbase/nf-winbase-deleteatom">DeleteAtom</a>



<a href="/windows/desktop/api/winbase/nf-winbase-findatoma">FindAtom</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getatomnamea">GetAtomName</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globaladdatoma">GlobalAddAtom</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globaldeleteatom">GlobalDeleteAtom</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globalfindatoma">GlobalFindAtom</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globalgetatomnamea">GlobalGetAtomName</a>



<b>Reference</b>