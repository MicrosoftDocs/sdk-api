---
UID: NF:lmat.NetScheduleJobEnum
title: NetScheduleJobEnum function
author: windows-sdk-content
description: The NetScheduleJobEnum function lists the jobs queued on a specified computer. This function requires that the schedule service be started.
old-location: netmgmt\netschedulejobenum.htm
tech.root: NetMgmt
ms.assetid: e3384414-6a15-4979-bed4-6f94f046474a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: NetScheduleJobEnum, NetScheduleJobEnum function [Network Management], _win32_netschedulejobenum, lmat/NetScheduleJobEnum, netmgmt.netschedulejobenum
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: lmat.h
req.include-header: Lmat.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetScheduleJobEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- NetScheduleJobEnum
: 
---

# NetScheduleJobEnum function


## -description


<p class="CCE_Message">[<b>NetScheduleJobEnum</b> is no longer available for use as of Windows 8. Instead, use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e"> Task Scheduler 2.0 Interfaces</a>.

]

The
				<b>NetScheduleJobEnum</b> function lists the jobs queued on a specified computer. This function requires that the schedule service be started. 


## -parameters




### -param Servername [in, optional]

A pointer to a constant string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.


### -param PointerToBuffer [out]

A pointer to the buffer that receives the data. The return information is an array of 
<a href="https://msdn.microsoft.com/ed7c5171-b8aa-4a9a-8f31-4d914bcad0b1">AT_ENUM</a> structures. The buffer is allocated by the system and must be freed using a single call to the 
<a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a> function. Note that you must free the buffer even if the function fails with ERROR_MORE_DATA.


### -param PrefferedMaximumLength [in]

A value that indicates the preferred maximum length of the returned data, in bytes. If you specify MAX_PREFERRED_LENGTH, the function allocates the amount of memory required for the data. If you specify another value in this parameter, it can restrict the number of bytes that the function returns. If the buffer size is insufficient to hold all entries, the function returns ERROR_MORE_DATA. For more information, see 
<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a> and 
<a href="https://msdn.microsoft.com/08599966-68a1-420b-bbc7-6daac833d08f">Network Management Function Buffer Lengths</a>.


### -param EntriesRead [out]

A pointer to a value that receives the count of elements actually enumerated.


### -param TotalEntries [out]

A pointer to a value that receives the total number of entries that could have been enumerated from the current resume position. Note that applications should consider this value only as a hint.


### -param ResumeHandle [in, out]

A pointer to a value that contains a resume handle which is used to continue a job enumeration. The handle should be zero on the first call and left unchanged for subsequent calls. If this parameter is <b>NULL</b>, then no resume handle is stored.


## -returns



If the function succeeds, the return value is NERR_Success.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



Normally only members of the local Administrators group on the computer where the schedule job is being enumerated can successfully execute this function. If the server name passed in the string pointed to by the <i>Servername</i> parameter is a remote server, then only members of the local Administrators group on the  server can successfully execute this function. 

If the following registry value has the least significant bit set (for example, 0x00000001), then users belonging to the Server Operators group can also successfully execute this function.


<b>HKLM\System\CurrentControlSet\Control\Lsa\SubmitControl</b>

Each entry returned contains an 
<a href="https://msdn.microsoft.com/ed7c5171-b8aa-4a9a-8f31-4d914bcad0b1">AT_ENUM</a> structure. The value of the <b>JobId</b> member can be used when calling functions that require a job identifier parameter, such as the 
<a href="https://msdn.microsoft.com/5ae668ab-f51d-457e-a239-2ec16a0e5a55">NetScheduleJobDel</a> function.




## -see-also




<a href="https://msdn.microsoft.com/ed7c5171-b8aa-4a9a-8f31-4d914bcad0b1">AT_ENUM</a>



<a href="https://msdn.microsoft.com/813d13ba-abe1-4b14-88c7-87ba88a42a3b">NetScheduleJobAdd</a>



<a href="https://msdn.microsoft.com/5ae668ab-f51d-457e-a239-2ec16a0e5a55">NetScheduleJobDel</a>



<a href="https://msdn.microsoft.com/44589715-edab-4737-9e49-6f491fd44c28">NetScheduleJobGetInfo</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>



<a href="https://msdn.microsoft.com/1ddc9b95-fdbc-4e39-9b55-2a5bc570b95d">Schedule
		  Functions</a>
 

 

