---
UID: NF:winbase.DeleteAtom
title: DeleteAtom function
author: windows-sdk-content
description: Decrements the reference count of a local string atom. If the atom's reference count is reduced to zero, DeleteAtom removes the string associated with the atom from the local atom table.
old-location: dataxchg\deleteatom.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\atoms\atomreference\atomfunctions\deleteatom.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: DeleteAtom, DeleteAtom function [Data Exchange], _win32_DeleteAtom, _win32_deleteatom_cpp, dataxchg.deleteatom, winbase/DeleteAtom, winui._win32_deleteatom
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
req.unicode-ansi: 
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
 - DeleteAtom
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DeleteAtom function


## -description


Decrements the reference count of a local string atom. If the atom's reference count is reduced to zero, <b>DeleteAtom</b> removes the string associated with the atom from the local atom table. 


## -parameters




### -param nAtom [in]

Type: <b>ATOM</b>

The atom to be deleted. 


## -returns



Type: <b>ATOM</b>

If the function succeeds, the return value is zero.

If the function fails, the return value is the 
						<i>nAtom</i> parameter. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



A string atom's reference count specifies the number of times the atom has been added to the atom table. The <a href="https://msdn.microsoft.com/en-us/library/ms649056(v=VS.85).aspx">AddAtom</a> function increments the count on each call. The <b>DeleteAtom</b> function decrements the count on each call but removes the string only if the atom's reference count is zero. 

Each call to <a href="https://msdn.microsoft.com/en-us/library/ms649056(v=VS.85).aspx">AddAtom</a> should have a corresponding call to <b>DeleteAtom</b>. Do not call <b>DeleteAtom</b> more times than you call <b>AddAtom</b>, or you may delete the atom while other clients are using it. 

The <b>DeleteAtom</b> function has no effect on an integer atom (an atom whose value is in the range 0x0001 to 0xBFFF). The function always returns zero for an integer atom. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms649056(v=VS.85).aspx">AddAtom</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649058(v=VS.85).aspx">FindAtom</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649060(v=VS.85).aspx">GlobalAddAtom</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649061(v=VS.85).aspx">GlobalDeleteAtom</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649062(v=VS.85).aspx">GlobalFindAtom</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649055(v=VS.85).aspx">MAKEINTATOM</a>



<b>Reference</b>
 

 

