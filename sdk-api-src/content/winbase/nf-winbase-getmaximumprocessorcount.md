---
UID: NF:winbase.GetMaximumProcessorCount
title: GetMaximumProcessorCount function (winbase.h)
author: windows-sdk-content
description: Returns the maximum number of logical processors that a processor group or the system can have.
old-location: base\getmaximumprocessorcount.htm
tech.root: ProcThread
ms.assetid: 71ce4fb4-ef63-4750-a842-bbfb1a5b0543
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetMaximumProcessorCount, GetMaximumProcessorCount function, base.getmaximumprocessorcount, winbase/GetMaximumProcessorCount
ms.topic: function
f1_keywords: 
 - "winbase/GetMaximumProcessorCount"
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
api_name:
 - GetMaximumProcessorCount
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetMaximumProcessorCount function


## -description


Returns the maximum number of logical processors that a processor group or the system can have.


## -parameters




### -param GroupNumber [in]

The processor group number. If this parameter is ALL_PROCESSOR_GROUPS, the function returns the maximum number of processors that the system can have. 


## -returns



If the function succeeds, the return value is the maximum number of processors that the specified group can have.

If the function fails, the return value is zero. To get extended error information, use <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



To compile an application that uses this function, set _WIN32_WINNT &gt;= 0x0601. For more information, see <a href="https://docs.microsoft.com/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.



