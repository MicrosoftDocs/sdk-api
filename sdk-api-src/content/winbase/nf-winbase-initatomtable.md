---
UID: NF:winbase.InitAtomTable
title: InitAtomTable function
author: windows-sdk-content
description: Initializes the local atom table and sets the number of hash buckets to the specified size.
old-location: dataxchg\initatomtable.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\atoms\atomreference\atomfunctions\initatomtable.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: InitAtomTable, InitAtomTable function [Data Exchange], _win32_InitAtomTable, _win32_initatomtable_cpp, dataxchg.initatomtable, winbase/InitAtomTable, winui._win32_initatomtable
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
 - InitAtomTable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/0712cd2e-397f-48e1-b3bd-ed0dd3155373">AddAtom</a>



<a href="https://msdn.microsoft.com/44c4fbdd-2206-4a6f-9bf1-5495407f6800">DeleteAtom</a>



<a href="https://msdn.microsoft.com/de8ca30a-9de0-4d56-b508-4d02d6eed562">FindAtom</a>



<a href="https://msdn.microsoft.com/50b01772-660c-4421-8a6f-a6da5369bad4">GetAtomName</a>



<a href="https://msdn.microsoft.com/890c8c69-5a8e-42be-9eaf-84f9ccaa7e3d">GlobalAddAtom</a>



<a href="https://msdn.microsoft.com/387f2dbf-39c3-4294-b77d-0439e296a000">GlobalDeleteAtom</a>



<a href="https://msdn.microsoft.com/1787e632-aae7-44d9-881e-847ca20b8981">GlobalFindAtom</a>



<a href="https://msdn.microsoft.com/7ba8ea4d-7efe-4eb3-afea-c84ab6cacaea">GlobalGetAtomName</a>



<b>Reference</b>
 

 

