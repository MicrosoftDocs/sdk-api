---
UID: NF:wtsapi32.WTSEnumerateProcessesW
title: WTSEnumerateProcessesW function (wtsapi32.h)
description: Retrieves information about the active processes on a specified Remote Desktop Session Host (RD Session Host) server. (Unicode)
helpviewer_keywords: ["WTSEnumerateProcesses", "WTSEnumerateProcesses function [Remote Desktop Services]", "WTSEnumerateProcessesW", "_win32_wtsenumerateprocesses", "termserv.wtsenumerateprocesses", "wtsapi32/WTSEnumerateProcesses", "wtsapi32/WTSEnumerateProcessesW"]
old-location: termserv\wtsenumerateprocesses.htm
tech.root: TermServ
ms.assetid: ddfae294-2e7c-416e-b328-76d011b4af39
ms.date: 12/05/2018
ms.keywords: WTSEnumerateProcesses, WTSEnumerateProcesses function [Remote Desktop Services], WTSEnumerateProcessesA, WTSEnumerateProcessesW, _win32_wtsenumerateprocesses, termserv.wtsenumerateprocesses, wtsapi32/WTSEnumerateProcesses, wtsapi32/WTSEnumerateProcessesA, wtsapi32/WTSEnumerateProcessesW
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WTSEnumerateProcessesW (Unicode) and WTSEnumerateProcessesA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WTSEnumerateProcessesW
 - wtsapi32/WTSEnumerateProcessesW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-session-wtsapi32-l1-1-1.dll
 - Wtsapi32.dll
 - Ext-MS-Win-Session-WtsApi32-l1-1-0.dll
api_name:
 - WTSEnumerateProcesses
 - WTSEnumerateProcessesA
 - WTSEnumerateProcessesW
req.apiset: ext-ms-win-session-wtsapi32-l1-1-0 (introduced in Windows 8)
---

# WTSEnumerateProcessesW function


## -description

Retrieves information about the active 
    processes on a specified Remote Desktop Session Host (RD Session Host) server.

## -parameters

### -param hServer [in]

Handle to an RD Session Host server. Specify a handle opened by the 
      <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsopenservera">WTSOpenServer</a> function, or specify 
      <b>WTS_CURRENT_SERVER_HANDLE</b> to indicate the RD Session Host server on which your application is 
      running.

### -param Reserved [in]

Reserved; must be zero.

### -param Version [in]

Specifies the version of the enumeration request. Must be 1.

### -param ppProcessInfo [out]

Pointer to a variable that receives a pointer to an array of 
      <a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_process_infoa">WTS_PROCESS_INFO</a> structures. Each structure 
      in the array contains information about an active process on the specified RD Session Host server. To free the returned 
      buffer, call the <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsfreememory">WTSFreeMemory</a> function.

### -param pCount [out]

Pointer to a variable that receives the number of <b>WTS_PROCESS_INFO</b> 
      structures returned in the <i>ppProcessInfo</i> buffer.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The caller must be a member of the Administrators group to enumerate processes that are running under a 
    different user's context.





> [!NOTE]
> The wtsapi32.h header defines WTSEnumerateProcesses as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_process_infoa">WTS_PROCESS_INFO</a>
