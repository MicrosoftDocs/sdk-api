---
UID: NF:winbase.GlobalAddAtomA
title: GlobalAddAtomA function
author: windows-sdk-content
description: Adds a character string to the global atom table and returns a unique value (an atom) identifying the string.
old-location: dataxchg\globaladdatom.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\atoms\atomreference\atomfunctions\globaladdatom.htm
ms.author: windowssdkdev
ms.date: 10/10/2018
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
---

# GlobalAddAtomA function


## -description


Adds a character string to the global atom table and returns a unique value (an atom) identifying the string. 


## -parameters




### -param lpString [in]

Type: <b>LPCTSTR</b>

The null-terminated string to be added. The string can have a maximum size of 255 bytes. Strings that differ only in case are considered identical. The case of the first string of this name added to the table is preserved and returned by the <a href="https://msdn.microsoft.com/7ba8ea4d-7efe-4eb3-afea-c84ab6cacaea">GlobalGetAtomName</a> function.

Alternatively, you can use an integer atom that has been converted using the <a href="https://msdn.microsoft.com/11270568-ef0e-4bed-9e07-cb62773178ff">MAKEINTATOM</a> macro. See the Remarks for more information. 


## -returns



Type: <b>ATOM</b>

If the function succeeds, the return value is the newly created atom.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



If the string already exists in the global atom table, the atom for the existing string is returned and the atom's reference count is incremented. 

The string associated with the atom is not deleted from memory until its reference count is zero. For more information, see the <a href="https://msdn.microsoft.com/387f2dbf-39c3-4294-b77d-0439e296a000">GlobalDeleteAtom</a> function. 

Global atoms are not deleted automatically when the application terminates. For every call to the <b>GlobalAddAtom</b> function, there must be a corresponding call to the <a href="https://msdn.microsoft.com/387f2dbf-39c3-4294-b77d-0439e296a000">GlobalDeleteAtom</a> function. 

If the 
				<i>lpString</i> parameter has the form "#1234", <b>GlobalAddAtom</b> returns an integer atom whose value is the 16-bit representation of the decimal number specified in the string (0x04D2, in this example). If the decimal value specified is 0x0000 or is greater than or equal to 0xC000, the return value is zero, indicating an error. If 
				<i>lpString</i> was created by the <a href="https://msdn.microsoft.com/11270568-ef0e-4bed-9e07-cb62773178ff">MAKEINTATOM</a> macro, the low-order word must be in the range 0x0001 through 0xBFFF. If the low-order word is not in this range, the function fails. 

If 
				<i>lpString</i> has any other form, <b>GlobalAddAtom</b> returns a string atom. 




## -see-also




<a href="https://msdn.microsoft.com/0712cd2e-397f-48e1-b3bd-ed0dd3155373">AddAtom</a>



<a href="https://msdn.microsoft.com/44c4fbdd-2206-4a6f-9bf1-5495407f6800">DeleteAtom</a>



<a href="https://msdn.microsoft.com/de8ca30a-9de0-4d56-b508-4d02d6eed562">FindAtom</a>



<a href="https://msdn.microsoft.com/50b01772-660c-4421-8a6f-a6da5369bad4">GetAtomName</a>



<a href="https://msdn.microsoft.com/387f2dbf-39c3-4294-b77d-0439e296a000">GlobalDeleteAtom</a>



<a href="https://msdn.microsoft.com/1787e632-aae7-44d9-881e-847ca20b8981">GlobalFindAtom</a>



<a href="https://msdn.microsoft.com/7ba8ea4d-7efe-4eb3-afea-c84ab6cacaea">GlobalGetAtomName</a>



<a href="https://msdn.microsoft.com/11270568-ef0e-4bed-9e07-cb62773178ff">MAKEINTATOM</a>



<b>Reference</b>
 

 

