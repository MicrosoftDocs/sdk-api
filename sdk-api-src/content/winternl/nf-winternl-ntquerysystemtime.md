---
UID: NF:winternl.NtQuerySystemTime
title: NtQuerySystemTime function
author: windows-sdk-content
description: Retrieves the current system time.
old-location: base\ntquerysystemtime.htm
tech.root: SysInfo
ms.assetid: 5b083c4f-ec2b-4118-b49e-1ca3e0af342e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: NtQuerySystemTime, NtQuerySystemTime function, base.ntquerysystemtime, winternl/NtQuerySystemTime
ms.topic: function
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
req.lib: 
req.dll: Ntdll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdll.dll
api_name:
 - NtQuerySystemTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NtQuerySystemTime function


## -description


<p class="CCE_Message">[<b>NtQuerySystemTime</b> may be altered or unavailable in future versions of Windows. Applications should use the <a href="https://msdn.microsoft.com/adf7ff5d-2d30-4490-9868-9ad78ef7a0b6">GetSystemTimeAsFileTime</a> function.]

Retrieves the current system time.


## -parameters




### -param SystemTime [out]

A pointer to a <a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a> structure that receives the system time. This is a 64-bit value representing the number of 100-nanosecond intervals since January 1, 1601 (UTC).


## -returns



If the function succeeds, it returns STATUS_SUCCESS.  If it fails, it will return the appropriate status code, which will typically be STATUS_ACCESS_VIOLATION.




## -remarks



This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Ntdll.dll.




## -see-also




<a href="https://msdn.microsoft.com/adf7ff5d-2d30-4490-9868-9ad78ef7a0b6">GetSystemTimeAsFileTime</a>



<a href="https://msdn.microsoft.com/3733f611-c6a1-4d48-b21e-ada3490c5de1">Time Functions</a>
 

 

