---
UID: NF:winbase.GlobalDeleteAtom
title: GlobalDeleteAtom function
author: windows-sdk-content
description: Decrements the reference count of a global string atom. If the atom's reference count reaches zero, GlobalDeleteAtom removes the string associated with the atom from the global atom table.
old-location: dataxchg\globaldeleteatom.htm
old-project: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\atoms\atomreference\atomfunctions\globaldeleteatom.htm
ms.author: windowssdkdev
ms.date: 05/17/2018
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
req.typenames: PRIORITY_HINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-atoms-l1-1-0.dll
-	kernel32legacy.dll
-	API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
api_name:
-	GlobalDeleteAtom
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



A string atom's reference count specifies the number of times the string has been added to the atom table. The <a href="https://msdn.microsoft.com/890c8c69-5a8e-42be-9eaf-84f9ccaa7e3d">GlobalAddAtom</a> function increments the reference count of a string that already exists in the global atom table each time it is called. 

Each call to <a href="https://msdn.microsoft.com/890c8c69-5a8e-42be-9eaf-84f9ccaa7e3d">GlobalAddAtom</a> should have a corresponding call to <b>GlobalDeleteAtom</b>. Do not call <b>GlobalDeleteAtom</b> more times than you call <b>GlobalAddAtom</b>, or you may delete the atom while other clients are using it. Applications using Dynamic Data Exchange (DDE) should follow the rules on global atom management to prevent leaks and premature deletion.

<b>GlobalDeleteAtom</b> has no effect on an integer atom (an atom whose value is in the range 0x0001 to 0xBFFF). The function always returns zero for an integer atom.


#### Examples

For an example, see <a href="using_dynamic_data_exchange.htm">Initiating a Conversation</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/0712cd2e-397f-48e1-b3bd-ed0dd3155373">AddAtom</a>



<a href="https://msdn.microsoft.com/44c4fbdd-2206-4a6f-9bf1-5495407f6800">DeleteAtom</a>



<a href="https://msdn.microsoft.com/de8ca30a-9de0-4d56-b508-4d02d6eed562">FindAtom</a>



<a href="https://msdn.microsoft.com/890c8c69-5a8e-42be-9eaf-84f9ccaa7e3d">GlobalAddAtom</a>



<a href="https://msdn.microsoft.com/1787e632-aae7-44d9-881e-847ca20b8981">GlobalFindAtom</a>



<a href="https://msdn.microsoft.com/11270568-ef0e-4bed-9e07-cb62773178ff">MAKEINTATOM</a>



<b>Reference</b>
 

 

