---
UID: NF:winbase.GetActiveProcessorCount
title: GetActiveProcessorCount function (winbase.h)
author: windows-sdk-content
description: Returns the number of active processors in a processor group or in the system.
old-location: base\getactiveprocessorcount.htm
tech.root: ProcThread
ms.assetid: f4ebb0a7-1c05-4478-85e3-80e6327ef8a4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetActiveProcessorCount, GetActiveProcessorCount function, base.getactiveprocessorcount, winbase/GetActiveProcessorCount
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
 - API-MS-Win-Core-processtopology-Obsolete-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-ProcessTopology-Obsolete-L1-1-1.dll
api_name:
 - GetActiveProcessorCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetActiveProcessorCount function


## -description


Returns the number of active processors in a processor group or in the system.


## -parameters




### -param GroupNumber [in]

The processor group number. If this parameter is ALL_PROCESSOR_GROUPS, the function returns the number of active processors in the system.


## -returns



If the function succeeds, the return value is the number of active processors in the specified group.

If the function fails, the return value is zero. To get extended error information, use <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To compile an application that uses this function, set _WIN32_WINNT &gt;= 0x0601. For more information, see <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.



