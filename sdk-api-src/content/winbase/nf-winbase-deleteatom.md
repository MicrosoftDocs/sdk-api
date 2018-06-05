---
UID: NF:winbase.DeleteAtom
title: DeleteAtom function
author: windows-sdk-content
description: Decrements the reference count of a local string atom. If the atom's reference count is reduced to zero, DeleteAtom removes the string associated with the atom from the local atom table.
old-location: dataxchg\deleteatom.htm
old-project: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\atoms\atomreference\atomfunctions\deleteatom.htm
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: DeleteAtom, DeleteAtom function [Data Exchange], _win32_DeleteAtom, _win32_deleteatom_cpp, dataxchg.deleteatom, winbase/DeleteAtom, winui._win32_deleteatom
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
-	DeleteAtom
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
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



A string atom's reference count specifies the number of times the atom has been added to the atom table. The <a href="https://msdn.microsoft.com/0712cd2e-397f-48e1-b3bd-ed0dd3155373">AddAtom</a> function increments the count on each call. The <b>DeleteAtom</b> function decrements the count on each call but removes the string only if the atom's reference count is zero. 

Each call to <a href="https://msdn.microsoft.com/0712cd2e-397f-48e1-b3bd-ed0dd3155373">AddAtom</a> should have a corresponding call to <b>DeleteAtom</b>. Do not call <b>DeleteAtom</b> more times than you call <b>AddAtom</b>, or you may delete the atom while other clients are using it. 

The <b>DeleteAtom</b> function has no effect on an integer atom (an atom whose value is in the range 0x0001 to 0xBFFF). The function always returns zero for an integer atom. 




## -see-also




<a href="https://msdn.microsoft.com/0712cd2e-397f-48e1-b3bd-ed0dd3155373">AddAtom</a>



<a href="https://msdn.microsoft.com/de8ca30a-9de0-4d56-b508-4d02d6eed562">FindAtom</a>



<a href="https://msdn.microsoft.com/890c8c69-5a8e-42be-9eaf-84f9ccaa7e3d">GlobalAddAtom</a>



<a href="https://msdn.microsoft.com/387f2dbf-39c3-4294-b77d-0439e296a000">GlobalDeleteAtom</a>



<a href="https://msdn.microsoft.com/1787e632-aae7-44d9-881e-847ca20b8981">GlobalFindAtom</a>



<a href="https://msdn.microsoft.com/11270568-ef0e-4bed-9e07-cb62773178ff">MAKEINTATOM</a>



<b>Reference</b>
 

 

