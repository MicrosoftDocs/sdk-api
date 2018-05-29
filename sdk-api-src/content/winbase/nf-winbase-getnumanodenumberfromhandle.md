---
UID: NF:winbase.GetNumaNodeNumberFromHandle
title: GetNumaNodeNumberFromHandle function
author: windows-sdk-content
description: Retrieves the NUMA node associated with the file or I/O device represented by the specified file handle.
old-location: base\getnumanodenumberfromhandle.htm
old-project: ProcThread
ms.assetid: 7622f7c9-2dfc-4ab7-b3e9-48d483c6cc0e
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: GetNumaNodeNumberFromHandle, GetNumaNodeNumberFromHandle function, base.getnumanodenumberfromhandle, winbase/GetNumaNodeNumberFromHandle
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
-	kernel32.dll
api_name:
-	GetNumaNodeNumberFromHandle
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetNumaNodeNumberFromHandle function


## -description


Retrieves the NUMA node associated with the file or I/O device represented by the specified file handle.


## -parameters




### -param hFile [in]

A handle to a file or I/O device. Examples of I/O devices include files, file streams, volumes, physical disks, and sockets. For more information, see the <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> function.


### -param NodeNumber [out]

A pointer to a variable to receive the number of the NUMA node associated with the specified file handle.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, use <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If the specified handle does not have a node associated with it, the function returns FALSE. The value of the <i>NodeNumber</i> parameter is undetermined and should not be used.

To compile an application that uses this function, set _WIN32_WINNT &gt;= 0x0601. For more information, see <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/a1263968-2b26-45cc-bdd7-6aa354821a5a">NUMA Support</a>
 

 

