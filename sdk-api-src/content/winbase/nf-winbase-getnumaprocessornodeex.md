---
UID: NF:winbase.GetNumaProcessorNodeEx
title: GetNumaProcessorNodeEx function
author: windows-sdk-content
description: Retrieves the node number as a USHORT value for the specified logical processor.
old-location: base\getnumaprocessornodeex.htm
tech.root: ProcThread
ms.assetid: 6b843cd8-eeb5-4aa1-aad4-ce98916346b1
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: GetNumaProcessorNodeEx, GetNumaProcessorNodeEx function, base.getnumaprocessornodeex, winbase/GetNumaProcessorNodeEx
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - GetNumaProcessorNodeEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetNumaProcessorNodeEx function


## -description


Retrieves the node number as a <b>USHORT</b> value for the specified logical processor.


## -parameters




### -param Processor [in]

A pointer to a <a href="https://msdn.microsoft.com/9005c6d4-07a9-4ce0-9ee2-54880d7244c3">PROCESSOR_NUMBER</a> structure that represents the logical processor and the processor group to which it is assigned.


### -param NodeNumber [out]

A pointer  to a variable to receive the node number. If the specified processor does not exist, this parameter is set to MAXUSHORT.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To compile an application that uses this function, set _WIN32_WINNT &gt;= 0x0601. For more information, see <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/88e6c6b3-7ec5-43e5-8cf3-21402925f718">GetNumaProcessorNode</a>



<a href="https://msdn.microsoft.com/9005c6d4-07a9-4ce0-9ee2-54880d7244c3">PROCESSOR_NUMBER</a>
 

 

