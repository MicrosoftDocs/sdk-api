---
UID: NF:winternl.NtQuerySystemTime
title: NtQuerySystemTime function (winternl.h)
description: Retrieves the current system time.
helpviewer_keywords: ["NtQuerySystemTime","NtQuerySystemTime function","base.ntquerysystemtime","winternl/NtQuerySystemTime"]
old-location: base\ntquerysystemtime.htm
tech.root: winprog
ms.assetid: 5b083c4f-ec2b-4118-b49e-1ca3e0af342e
ms.date: 12/05/2018
ms.keywords: NtQuerySystemTime, NtQuerySystemTime function, base.ntquerysystemtime, winternl/NtQuerySystemTime
req.header: winternl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ntdll.lib
req.dll: ntdll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NtQuerySystemTime
 - winternl/NtQuerySystemTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdll.dll
api_name:
 - NtQuerySystemTime
---

# NtQuerySystemTime function


## -description

<p class="CCE_Message">[<b>NtQuerySystemTime</b> may be altered or unavailable in future versions of Windows. Applications should use the <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime">GetSystemTimeAsFileTime</a> function.]

Retrieves the current system time.

## -parameters

### -param SystemTime [out]

A pointer to a <a href="/windows/win32/api/winnt/ns-winnt-large_integer-r1">LARGE_INTEGER</a> structure that receives the system time. This is a 64-bit value representing the number of 100-nanosecond intervals since January 1, 1601 (UTC).

## -returns

If the function succeeds, it returns STATUS_SUCCESS.  If it fails, it will return the appropriate status code, which will typically be STATUS_ACCESS_VIOLATION.

## -remarks

This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Ntdll.dll.

## -see-also

<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime">GetSystemTimeAsFileTime</a>



<a href="/windows/desktop/SysInfo/time-functions">Time Functions</a>