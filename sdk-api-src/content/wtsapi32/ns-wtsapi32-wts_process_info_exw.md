---
UID: NS:wtsapi32._WTS_PROCESS_INFO_EXW
title: WTS_PROCESS_INFO_EXW (wtsapi32.h)
description: Contains extended information about a process running on a Remote Desktop Session Host (RD Session Host) server. (Unicode)
helpviewer_keywords: ["*PWTS_PROCESS_INFO_EXW","PWTS_PROCESS_INFO_EX","PWTS_PROCESS_INFO_EX structure pointer [Remote Desktop Services]","WTS_PROCESS_INFO_EX","WTS_PROCESS_INFO_EX structure [Remote Desktop Services]","WTS_PROCESS_INFO_EXA","WTS_PROCESS_INFO_EXW","termserv.wts_process_info_ex","wtsapi32/PWTS_PROCESS_INFO_EX","wtsapi32/WTS_PROCESS_INFO_EX","wtsapi32/WTS_PROCESS_INFO_EXA","wtsapi32/WTS_PROCESS_INFO_EXW"]
old-location: termserv\wts_process_info_ex.htm
tech.root: TermServ
ms.assetid: a678d249-4943-4d2b-9cea-87ce20177c75
ms.date: 12/05/2018
ms.keywords: '*PWTS_PROCESS_INFO_EXW, PWTS_PROCESS_INFO_EX, PWTS_PROCESS_INFO_EX structure pointer [Remote Desktop Services], WTS_PROCESS_INFO_EX, WTS_PROCESS_INFO_EX structure [Remote Desktop Services], WTS_PROCESS_INFO_EXA, WTS_PROCESS_INFO_EXW, termserv.wts_process_info_ex, wtsapi32/PWTS_PROCESS_INFO_EX, wtsapi32/WTS_PROCESS_INFO_EX, wtsapi32/WTS_PROCESS_INFO_EXA, wtsapi32/WTS_PROCESS_INFO_EXW'
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WTS_PROCESS_INFO_EXW (Unicode) and WTS_PROCESS_INFO_EXA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WTS_PROCESS_INFO_EXW, *PWTS_PROCESS_INFO_EXW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WTS_PROCESS_INFO_EXW
 - wtsapi32/_WTS_PROCESS_INFO_EXW
 - PWTS_PROCESS_INFO_EXW
 - wtsapi32/PWTS_PROCESS_INFO_EXW
 - WTS_PROCESS_INFO_EXW
 - wtsapi32/WTS_PROCESS_INFO_EXW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wtsapi32.h
api_name:
 - WTS_PROCESS_INFO_EX
 - WTS_PROCESS_INFO_EXA
 - WTS_PROCESS_INFO_EXW
---

# WTS_PROCESS_INFO_EXW structure


## -description

Contains extended information about a process running on a Remote Desktop Session Host (RD Session Host) server. This structure is returned by the <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesexa">WTSEnumerateProcessesEx</a> function when you set the <i>pLevel</i> parameter to one.

## -struct-fields

### -field SessionId

The Remote Desktop Services session identifier for the session associated with the process.

### -field ProcessId

The process identifier that uniquely identifies the process on the RD Session Host server.

### -field pProcessName

A pointer to a null-terminated string that contains the name of the executable file associated with the process.

### -field pUserSid

A pointer to the user security identifiers (SIDs) in the primary access token of the process. For more 
      information about SIDs and access tokens, see 
      <a href="/windows/desktop/SecAuthZ/access-control">Access Control</a> and 
      <a href="/windows/desktop/SecAuthZ/security-identifiers">Security Identifiers</a>.

### -field NumberOfThreads

The number of threads in the process.

### -field HandleCount

The number of handles in the process.

### -field PagefileUsage

The page file usage of the process, in bytes.

### -field PeakPagefileUsage

The peak page file usage of the process, in bytes.

### -field WorkingSetSize

The working set size of the process, in bytes.

### -field PeakWorkingSetSize

The peak working set size of the process, in bytes.

### -field UserTime

The amount of time, in milliseconds, the process has been running in user mode.

### -field KernelTime

The amount of time, in milliseconds, the process has been running in kernel mode.

## -see-also

<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa">WTSEnumerateProcesses</a>



<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesexa">WTSEnumerateProcessesEx</a>



<a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_process_infoa">WTS_PROCESS_INFO</a>

## -remarks

> [!NOTE]
> The wtsapi32.h header defines WTS_PROCESS_INFO_EX as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
