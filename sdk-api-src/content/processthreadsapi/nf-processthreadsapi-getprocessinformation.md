---
UID: NF:processthreadsapi.GetProcessInformation
title: GetProcessInformation function
author: windows-sdk-content
description: Retrieves information about the specified process.
old-location: base\getprocessinformation.htm
tech.root: procthread
ms.assetid: 2b075405-b7b6-4da0-b78d-45eaa9c6c8cd
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: GetProcessInformation, GetProcessInformation function, base.getprocessinformation, processthreadsapi/GetProcessInformation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: processthreadsapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - Kernel32.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
 - KernelBase.dll
api_name:
 - GetProcessInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetProcessInformation function


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Retrieves information about the specified process.


## -parameters




### -param hProcess [in]

A handle to the process. This handle must have the <b>PROCESS_SET_INFORMATION</b> access 
     right. For more information, see 
     <a href="https://msdn.microsoft.com/508a17c4-88cd-431a-a102-00180a7f7ab5">Process Security and Access Rights</a>.


### -param ProcessInformationClass [in]

The kind of information to retrieve.


### -param ProcessInformation

Pointer to an object to receive the type of information specified by the 
       <i>ProcessInformationClass</i> parameter.

If the <i>ProcessInformationClass</i> parameter is 
       <b>ProcessMemoryPriority</b>, this parameter must point to a 
       <a href="https://msdn.microsoft.com/03cacfdf-5c66-42e4-bfcf-afaacd3ad038">MEMORY_PRIORITY_INFORMATION</a> structure.

If the <i>ProcessInformationClass</i> parameter is 
       <b>ProcessPowerThrottling</b>, this parameter must point to a 
       <a href="https://msdn.microsoft.com/394B6509-849C-4B4C-9A46-AF5011A03585">PROCESS_POWER_THROTTLING_STATE</a> structure.

If the <i>ProcessInformationClass</i> parameter is 
       <b>ProcessProtectionLevelInfo</b>, this parameter must point to a 
       <a href="https://msdn.microsoft.com/E2A99AB0-33F1-4AF5-A05B-31D0929D9B4B">PROCESS_PROTECTION_LEVEL_INFORMATION</a> structure.

If the <i>ProcessInformationClass</i> parameter is 
       <b>ProcessLeapSecondInfo</b>, this parameter must point to a 
       <a href="base.process_leap_second_info">PROCESS_LEAP_SECOND_INFO</a> structure.

If the <i>ProcessInformationClass</i> parameter is 
       <b>ProcessAppMemoryInfo</b>, this parameter must point to a 
       <a href="https://msdn.microsoft.com/A2D0CDED-0E8B-41D6-8435-BDB4E5445DE4">APP_MEMORY_INFORMATION</a> structure.


### -param ProcessInformationSize [in]

The size in bytes of the structure specified by the <i>ProcessInformation</i> parameter.

If the <i>ProcessInformationClass</i> parameter is 
      <b>ProcessMemoryPriority</b>, this parameter must be 
      <code>sizeof(MEMORY_PRIORITY_INFORMATION)</code>.

If the <i>ProcessInformationClass</i> parameter is 
       <b>ProcessPowerThrottling</b>, this parameter must be 
       <code>sizeof(PROCESS_POWER_THROTTLING_STATE)</code>.

If the <i>ProcessInformationClass</i> parameter is 
       <b>ProcessProtectionLevelInfo</b>, this parameter must be 
       <code>sizeof(PROCESS_PROTECTION_LEVEL_INFORMATION)</code>.

If the <i>ProcessInformationClass</i> parameter is 
       <b>ProcessLeapSecondInfo</b>, this parameter must be 
       <code>sizeof(PROCESS_LEAP_SECOND_INFO)</code>.

If the <i>ProcessInformationClass</i> parameter is 
       <b>ProcessAppMemoryInfo</b>, this parameter must be 
       <code>sizeof(APP_MEMORY_INFORMATION)</code>.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
      <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/b7996647-78ab-4f32-bcf6-41aa87d13bb8">GetThreadInformation</a>



<a href="https://msdn.microsoft.com/03cacfdf-5c66-42e4-bfcf-afaacd3ad038">MEMORY_PRIORITY_INFORMATION</a>



<a href="https://msdn.microsoft.com/4A09E341-82FB-4E50-B2DD-EEDE443F3F1E">PROCESS_INFORMATION_CLASS</a>



<a href="https://msdn.microsoft.com/1739fadf-6b43-4b89-8a17-87d9867d5197">SetProcessInformation</a>
 

 

