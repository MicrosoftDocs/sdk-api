---
UID: NF:winternl.RtlTimeToSecondsSince1970
title: RtlTimeToSecondsSince1970 function
author: windows-sdk-content
description: Converts the specified 64-bit system time to the number of seconds since the beginning of January 1, 1970.
old-location: base\rtltimetosecondssince1970.htm
old-project: SysInfo
ms.assetid: cb2e041a-cbbb-4572-85da-b282fa692261
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: RtlTimeToSecondsSince1970, RtlTimeToSecondsSince1970 function, base.rtltimetosecondssince1970, winternl/RtlTimeToSecondsSince1970
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SYNC_VERSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdll.dll
api_name:
 - RtlTimeToSecondsSince1970
product: Windows
targetos: Windows
req.lib: 
req.dll: Ntdll.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# RtlTimeToSecondsSince1970 function


## -description


<p class="CCE_Message">[<b>RtlTimeToSecondsSince1970</b> is available for use in Windows 2000 and Windows XP.  It may be unavailable or modified in subsequent releases.]

Converts the specified 64-bit system time to the
    number of seconds since the beginning of January 1, 1970.


## -parameters




### -param Time [in]

A pointer to a <a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a> structure that specifies the system time. The valid years for this value are 1970 to  2105 inclusive.


### -param ElapsedSeconds [out]

A pointer to a variable that receives the number of seconds.


## -returns



If the function succeeds, it returns <b>TRUE</b>. If it fails, it returns <b>FALSE</b>. Typically, this function will fail if the specified value of the  <i>Time</i> parameter is not within the valid timeframe specified in the parameter description.




## -remarks



This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Ntdll.dll.

There is no single equivalent public  function. To perform this task using public  functions, use the following steps:



<ol>
<li>Call  <a href="https://msdn.microsoft.com/d19594bc-8238-4a8f-882d-5b9019ef4880">SystemTimeToFileTime</a> to copy the system time to a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure. Call <a href="https://msdn.microsoft.com/9ed8386b-f035-446f-b0f8-12e0d3f23aac">GetSystemTime</a> to get the current system time to pass to <b>SystemTimeToFileTime</b>.</li>
<li>Copy the contents of the <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure to a <a href="https://msdn.microsoft.com/83a10c12-2cd1-449a-af3f-b2138fc50ee0">ULARGE_INTEGER</a> structure.</li>
<li>Initialize a <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure with the date and time of the first second of January 1, 1970.</li>
<li>Call <a href="https://msdn.microsoft.com/d19594bc-8238-4a8f-882d-5b9019ef4880">SystemTimeToFileTime</a>, passing the <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure initialized in Step 3 to the call.</li>
<li>Copy the contents of the <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure returned by <a href="https://msdn.microsoft.com/d19594bc-8238-4a8f-882d-5b9019ef4880">SystemTimeToFileTime</a> in Step 4 to a second <a href="https://msdn.microsoft.com/83a10c12-2cd1-449a-af3f-b2138fc50ee0">ULARGE_INTEGER</a>.
The copied value should be less than or equal to the value copied in Step 2.</li>
<li>Subtract the 64-bit value in the <a href="https://msdn.microsoft.com/83a10c12-2cd1-449a-af3f-b2138fc50ee0">ULARGE_INTEGER</a> structure initialized in Step 5 (January 1, 1970) from the 64-bit value of the <b>ULARGE_INTEGER</b> structure initialized in Step 2 (the current system time). This produces a value in 100-nanosecond intervals since January 1, 1970. To convert this value to seconds, divide by 10,000,000.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a>



<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a>



<a href="https://msdn.microsoft.com/d19594bc-8238-4a8f-882d-5b9019ef4880">SystemTimeToFileTime</a>



<a href="https://msdn.microsoft.com/3733f611-c6a1-4d48-b21e-ada3490c5de1">Time Functions</a>



<a href="https://msdn.microsoft.com/83a10c12-2cd1-449a-af3f-b2138fc50ee0">ULARGE_INTEGER</a>
 

 

