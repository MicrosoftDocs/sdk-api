---
UID: NF:winbase.GlobalFindAtomW
title: GlobalFindAtomW function
author: windows-driver-content
description: Searches the global atom table for the specified character string and retrieves the global atom associated with that string.
old-location: dataxchg\globalfindatom.htm
old-project: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\atoms\atomreference\atomfunctions\globalfindatom.htm
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GlobalFindAtom, GlobalFindAtom function [Data Exchange], GlobalFindAtomA, GlobalFindAtomW, _win32_GlobalFindAtom, _win32_globalfindatom_cpp, dataxchg.globalfindatom, winbase/GlobalFindAtom, winbase/GlobalFindAtomA, winbase/GlobalFindAtomW, winui._win32_globalfindatom
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
req.unicode-ansi: GlobalFindAtomW (Unicode) and GlobalFindAtomA (ANSI)
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
-	GlobalFindAtom
-	GlobalFindAtomA
-	GlobalFindAtomW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GlobalFindAtomW function


## -description


Searches the global atom table for the specified character string and retrieves the global atom associated with that string. 


## -parameters




### -param lpString [in]

Type: <b>LPCTSTR</b>

The null-terminated character string for which to search. 

Alternatively, you can use an integer atom that has been converted using the <a href="https://msdn.microsoft.com/11270568-ef0e-4bed-9e07-cb62773178ff">MAKEINTATOM</a> macro. See the Remarks for more information. 


## -returns



Type: <b>ATOM</b>

If the function succeeds, the return value is the global atom associated with the given string.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



Even though the system preserves the case of a string in an atom table as it was originally entered, the search performed by <b>GlobalFindAtom</b> is not case sensitive. 

If 
				<i>lpString</i> was created by the <a href="https://msdn.microsoft.com/11270568-ef0e-4bed-9e07-cb62773178ff">MAKEINTATOM</a> macro, the low-order word must be in the range 0x0001 through 0xBFFF. If the low-order word is not in this range, the function fails. 




## -see-also




<a href="https://msdn.microsoft.com/0712cd2e-397f-48e1-b3bd-ed0dd3155373">AddAtom</a>



<a href="https://msdn.microsoft.com/44c4fbdd-2206-4a6f-9bf1-5495407f6800">DeleteAtom</a>



<a href="https://msdn.microsoft.com/de8ca30a-9de0-4d56-b508-4d02d6eed562">FindAtom</a>



<a href="https://msdn.microsoft.com/50b01772-660c-4421-8a6f-a6da5369bad4">GetAtomName</a>



<a href="https://msdn.microsoft.com/890c8c69-5a8e-42be-9eaf-84f9ccaa7e3d">GlobalAddAtom</a>



<a href="https://msdn.microsoft.com/387f2dbf-39c3-4294-b77d-0439e296a000">GlobalDeleteAtom</a>



<a href="https://msdn.microsoft.com/7ba8ea4d-7efe-4eb3-afea-c84ab6cacaea">GlobalGetAtomName</a>



<b>Reference</b>
 

 

