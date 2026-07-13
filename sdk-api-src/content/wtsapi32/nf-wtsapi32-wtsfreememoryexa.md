---
UID: NF:wtsapi32.WTSFreeMemoryExA
title: WTSFreeMemoryExA function (wtsapi32.h)
description: Frees memory that contains WTS_PROCESS_INFO_EX or WTS_SESSION_INFO_1 structures allocated by a Remote Desktop Services function. (ANSI)
helpviewer_keywords: ["WTSFreeMemoryExA", "wtsapi32/WTSFreeMemoryExA"]
old-location: termserv\wtsfreememoryex.htm
tech.root: TermServ
ms.assetid: d84a4fe3-a829-4cf3-b217-157391d0c495
ms.date: 12/05/2018
ms.keywords: WTSFreeMemoryEx, WTSFreeMemoryEx function [Remote Desktop Services], WTSFreeMemoryExA, WTSFreeMemoryExW, termserv.wtsfreememoryex, wtsapi32/WTSFreeMemoryEx, wtsapi32/WTSFreeMemoryExA, wtsapi32/WTSFreeMemoryExW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WTSFreeMemoryExA
 - wtsapi32/WTSFreeMemoryExA
dev_langs:
 - c++
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
req.apiset: ext-ms-win-session-wtsapi32-l1-1-0 (introduced in Windows 8)
---

# WTSFreeMemoryExA function


## -description

Frees memory that contains 
     <a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_process_info_exa">WTS_PROCESS_INFO_EX</a> or 
     <a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_session_info_1a">WTS_SESSION_INFO_1</a> structures allocated by a 
     Remote Desktop Services function.

## -parameters

### -param WTSTypeClass [in]

A value of the <a href="/windows/desktop/api/wtsapi32/ne-wtsapi32-wts_type_class">WTS_TYPE_CLASS</a> enumeration type 
      that specifies the type of structures contained in the buffer referenced by the 
      <i>pMemory</i> parameter.

### -param pMemory [in]

A pointer to the buffer to free.

### -param NumberOfEntries [in]

The number of elements in the buffer referenced by the <i>pMemory</i> parameter.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

Several Remote Desktop Services functions allocate buffers to return information. To free buffers that 
    contain <a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_process_info_exa">WTS_PROCESS_INFO_EX</a> or 
    <a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_session_info_1a">WTS_SESSION_INFO_1</a> structures, you must call the 
    <b>WTSFreeMemoryEx</b> function. To free other buffers, 
    you can call either the <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsfreememory">WTSFreeMemory</a> function or 
    the <b>WTSFreeMemoryEx</b> function.





> [!NOTE]
> The wtsapi32.h header defines WTSFreeMemoryEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa">WTSEnumerateProcesses </a>



<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesexa">WTSEnumerateProcessesEx</a>



<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsenumeratesessionsa">WTSEnumerateSessions</a>



<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsfreememory">WTSFreeMemory</a>



<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsquerysessioninformationa">WTSQuerySessionInformation</a>



<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsqueryuserconfiga">WTSQueryUserConfig</a>



<a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_process_info_exa">WTS_PROCESS_INFO_EX</a>



<a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_session_info_1a">WTS_SESSION_INFO_1</a>
