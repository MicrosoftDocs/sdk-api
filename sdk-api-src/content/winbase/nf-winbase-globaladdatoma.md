---
UID: NF:winbase.GlobalAddAtomA
title: GlobalAddAtomA function
author: windows-sdk-content
description: Adds a character string to the global atom table and returns a unique value (an atom) identifying the string.
old-location: dataxchg\globaladdatom.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\atoms\atomreference\atomfunctions\globaladdatom.htm
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: GlobalAddAtom, GlobalAddAtom function [Data Exchange], GlobalAddAtomA, GlobalAddAtomW, _win32_GlobalAddAtom, _win32_globaladdatom_cpp, dataxchg.globaladdatom, winbase/GlobalAddAtom, winbase/GlobalAddAtomA, winbase/GlobalAddAtomW, winui._win32_globaladdatom
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GlobalAddAtomW (Unicode) and GlobalAddAtomA (ANSI)
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
 - GlobalAddAtom
 - GlobalAddAtomA
 - GlobalAddAtomW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- GlobalAddAtomA
: 
---

# GlobalAddAtomA function


## -description


Adds a character string to the global atom table and returns a unique value (an atom) identifying the string. 


## -parameters




### -param lpString [in]

Type: <b>LPCTSTR</b>

The null-terminated string to be added. The string can have a maximum size of 255 bytes. Strings that differ only in case are considered identical. The case of the first string of this name added to the table is preserved and returned by the <a href="https://msdn.microsoft.com/en-us/library/ms649063(v=VS.85).aspx">GlobalGetAtomName</a> function.

Alternatively, you can use an integer atom that has been converted using the <a href="https://msdn.microsoft.com/en-us/library/ms649055(v=VS.85).aspx">MAKEINTATOM</a> macro. See the Remarks for more information. 


## -returns



Type: <b>ATOM</b>

If the function succeeds, the return value is the newly created atom.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



If the string already exists in the global atom table, the atom for the existing string is returned and the atom's reference count is incremented. 

The string associated with the atom is not deleted from memory until its reference count is zero. For more information, see the <a href="https://msdn.microsoft.com/en-us/library/ms649061(v=VS.85).aspx">GlobalDeleteAtom</a> function. 

Global atoms are not deleted automatically when the application terminates. For every call to the <b>GlobalAddAtom</b> function, there must be a corresponding call to the <a href="https://msdn.microsoft.com/en-us/library/ms649061(v=VS.85).aspx">GlobalDeleteAtom</a> function. 

If the 
				<i>lpString</i> parameter has the form "#1234", <b>GlobalAddAtom</b> returns an integer atom whose value is the 16-bit representation of the decimal number specified in the string (0x04D2, in this example). If the decimal value specified is 0x0000 or is greater than or equal to 0xC000, the return value is zero, indicating an error. If 
				<i>lpString</i> was created by the <a href="https://msdn.microsoft.com/en-us/library/ms649055(v=VS.85).aspx">MAKEINTATOM</a> macro, the low-order word must be in the range 0x0001 through 0xBFFF. If the low-order word is not in this range, the function fails. 

If 
				<i>lpString</i> has any other form, <b>GlobalAddAtom</b> returns a string atom. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms649056(v=VS.85).aspx">AddAtom</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649057(v=VS.85).aspx">DeleteAtom</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649058(v=VS.85).aspx">FindAtom</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649059(v=VS.85).aspx">GetAtomName</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649061(v=VS.85).aspx">GlobalDeleteAtom</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649062(v=VS.85).aspx">GlobalFindAtom</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649063(v=VS.85).aspx">GlobalGetAtomName</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649055(v=VS.85).aspx">MAKEINTATOM</a>



<b>Reference</b>
 

 

