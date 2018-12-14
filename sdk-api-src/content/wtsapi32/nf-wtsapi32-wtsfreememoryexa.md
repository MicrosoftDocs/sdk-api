---
UID: NF:wtsapi32.WTSFreeMemoryExA
title: WTSFreeMemoryExA function
author: windows-sdk-content
description: Frees memory that contains WTS_PROCESS_INFO_EX or WTS_SESSION_INFO_1 structures allocated by a Remote Desktop Services function.
old-location: termserv\wtsfreememoryex.htm
tech.root: TermServ
ms.assetid: d84a4fe3-a829-4cf3-b217-157391d0c495
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WTSFreeMemoryEx, WTSFreeMemoryEx function [Remote Desktop Services], WTSFreeMemoryExA, WTSFreeMemoryExW, termserv.wtsfreememoryex, wtsapi32/WTSFreeMemoryEx, wtsapi32/WTSFreeMemoryExA, wtsapi32/WTSFreeMemoryExW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WTSFreeMemoryExW (Unicode) and WTSFreeMemoryExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wtsapi32.dll
 - Ext-MS-Win-Session-WtsApi32-l1-1-0.dll
api_name:
 - WTSFreeMemoryEx
 - WTSFreeMemoryExA
 - WTSFreeMemoryExW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WTSFreeMemoryExA function


## -description


Frees memory that contains 
     <a href="https://msdn.microsoft.com/a678d249-4943-4d2b-9cea-87ce20177c75">WTS_PROCESS_INFO_EX</a> or 
     <a href="https://msdn.microsoft.com/29d76033-d61d-4bc5-b47a-f7dea9543f23">WTS_SESSION_INFO_1</a> structures allocated by a 
     Remote Desktop Services function.


## -parameters




### -param WTSTypeClass [in]

A value of the <a href="https://msdn.microsoft.com/1827e862-add0-4271-b5d7-62834c396250">WTS_TYPE_CLASS</a> enumeration type 
      that specifies the type of structures contained in the buffer referenced by the 
      <i>pMemory</i> parameter.


### -param pMemory [in]

A pointer to the buffer to free.


### -param NumberOfEntries [in]

The number of elements in the buffer referenced by the <i>pMemory</i> parameter.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -remarks



Several Remote Desktop Services functions allocate buffers to return information. To free buffers that 
    contain <a href="https://msdn.microsoft.com/a678d249-4943-4d2b-9cea-87ce20177c75">WTS_PROCESS_INFO_EX</a> or 
    <a href="https://msdn.microsoft.com/29d76033-d61d-4bc5-b47a-f7dea9543f23">WTS_SESSION_INFO_1</a> structures, you must call the 
    <b>WTSFreeMemoryEx</b> function. To free other buffers, 
    you can call either the <a href="https://msdn.microsoft.com/1c325174-ec08-4bbb-8e91-1a3cc9256110">WTSFreeMemory</a> function or 
    the <b>WTSFreeMemoryEx</b> function.




## -see-also




<a href="https://msdn.microsoft.com/ddfae294-2e7c-416e-b328-76d011b4af39">WTSEnumerateProcesses </a>



<a href="https://msdn.microsoft.com/bc8a2550-cf89-4203-b96b-c750c0dff255">WTSEnumerateProcessesEx</a>



<a href="https://msdn.microsoft.com/6f9dd7d4-48dc-411c-85f1-cd1239d1e106">WTSEnumerateSessions</a>



<a href="https://msdn.microsoft.com/1c325174-ec08-4bbb-8e91-1a3cc9256110">WTSFreeMemory</a>



<a href="https://msdn.microsoft.com/d52345a4-0408-4ea9-ba71-349910143752">WTSQuerySessionInformation</a>



<a href="https://msdn.microsoft.com/aabbcc03-3241-49ab-ab11-ccd3e6893e78">WTSQueryUserConfig</a>



<a href="https://msdn.microsoft.com/a678d249-4943-4d2b-9cea-87ce20177c75">WTS_PROCESS_INFO_EX</a>



<a href="https://msdn.microsoft.com/29d76033-d61d-4bc5-b47a-f7dea9543f23">WTS_SESSION_INFO_1</a>
 

 

