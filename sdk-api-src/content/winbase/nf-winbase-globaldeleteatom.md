---
UID: NF:winbase.GlobalDeleteAtom
title: GlobalDeleteAtom function
author: windows-sdk-content
description: Decrements the reference count of a global string atom. If the atom's reference count reaches zero, GlobalDeleteAtom removes the string associated with the atom from the global atom table.
old-location: dataxchg\globaldeleteatom.htm
old-project: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\atoms\atomreference\atomfunctions\globaldeleteatom.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GlobalDeleteAtom, GlobalDeleteAtom function [Data Exchange], _win32_GlobalDeleteAtom, _win32_globaldeleteatom_cpp, dataxchg.globaldeleteatom, winbase/GlobalDeleteAtom, winui._win32_globaldeleteatom
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: PRIORITY_HINT
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
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
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

To determine whether the function has failed, call <a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a> with <b>ERROR_SUCCESS</b> before calling <b>GlobalDeleteAtom</b>, then call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. If the last error code is still <b>ERROR_SUCCESS</b>, <b>GlobalDeleteAtom</b> has succeeded.




## -remarks



A string atom's reference count specifies the number of times the string has been added to the atom table. The <a href="https://msdn.microsoft.com/en-us/library/ms649060(v=VS.85).aspx">GlobalAddAtom</a> function increments the reference count of a string that already exists in the global atom table each time it is called. 

Each call to <a href="https://msdn.microsoft.com/en-us/library/ms649060(v=VS.85).aspx">GlobalAddAtom</a> should have a corresponding call to <b>GlobalDeleteAtom</b>. Do not call <b>GlobalDeleteAtom</b> more times than you call <b>GlobalAddAtom</b>, or you may delete the atom while other clients are using it. Applications using Dynamic Data Exchange (DDE) should follow the rules on global atom management to prevent leaks and premature deletion.

<b>GlobalDeleteAtom</b> has no effect on an integer atom (an atom whose value is in the range 0x0001 to 0xBFFF). The function always returns zero for an integer atom.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/en-us/library/ms648775(v=VS.85).aspx">Initiating a Conversation</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms649056(v=VS.85).aspx">AddAtom</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649057(v=VS.85).aspx">DeleteAtom</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649058(v=VS.85).aspx">FindAtom</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649060(v=VS.85).aspx">GlobalAddAtom</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649062(v=VS.85).aspx">GlobalFindAtom</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649055(v=VS.85).aspx">MAKEINTATOM</a>



<b>Reference</b>
 

 

