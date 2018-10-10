---
UID: NF:winternl.RtlLocalTimeToSystemTime
title: RtlLocalTimeToSystemTime function
author: windows-sdk-content
description: Converts the specified local time to system time.
old-location: base\rtllocaltimetosystemtime.htm
tech.root: SysInfo
ms.assetid: ce6f0578-0ea1-4e31-98a7-0008795abd32
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: RtlLocalTimeToSystemTime, RtlLocalTimeToSystemTime function, base.rtllocaltimetosystemtime, winternl/RtlLocalTimeToSystemTime
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - RtlLocalTimeToSystemTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtlLocalTimeToSystemTime function


## -description


<p class="CCE_Message">[<b>RtlLocalTimeToSystemTime</b> is available for use in Windows 2000 and Windows XP. It may be unavailable or modifed in subsequent releases. Applications should use the <a href="https://msdn.microsoft.com/491e4724-8e6f-4155-b427-15cd7968e2da">LocalFileTimeToFileTime</a> function.]

Converts the specified local time to system time.


## -parameters




### -param LocalTime [in]

A pointer to a <a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a> structure that specifies the local time.


### -param SystemTime [out]

A pointer to a <a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a> structure that receives the returned system time.


## -returns



If the function succeeds, it returns STATUS_SUCCESS.  If it fails, it will return the appropriate status code.




## -remarks



This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Ntdll.dll.




## -see-also




<a href="https://msdn.microsoft.com/491e4724-8e6f-4155-b427-15cd7968e2da">LocalFileTimeToFileTime</a>



<a href="https://msdn.microsoft.com/3733f611-c6a1-4d48-b21e-ada3490c5de1">Time Functions</a>
 

 

