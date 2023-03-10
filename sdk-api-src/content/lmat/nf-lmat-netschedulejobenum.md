---
UID: NF:lmat.NetScheduleJobEnum
title: NetScheduleJobEnum function (lmat.h)
description: The NetScheduleJobEnum function lists the jobs queued on a specified computer. This function requires that the schedule service be started.
helpviewer_keywords: ["NetScheduleJobEnum","NetScheduleJobEnum function [Network Management]","_win32_netschedulejobenum","lmat/NetScheduleJobEnum","netmgmt.netschedulejobenum"]
old-location: netmgmt\netschedulejobenum.htm
tech.root: NetMgmt
ms.assetid: e3384414-6a15-4979-bed4-6f94f046474a
ms.date: 12/05/2018
ms.keywords: NetScheduleJobEnum, NetScheduleJobEnum function [Network Management], _win32_netschedulejobenum, lmat/NetScheduleJobEnum, netmgmt.netschedulejobenum
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetScheduleJobEnum
 - lmat/NetScheduleJobEnum
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetScheduleJobEnum
---

# NetScheduleJobEnum function


## -description

<p class="CCE_Message">[<b>NetScheduleJobEnum</b> is no longer available for use as of Windows 8. Instead, use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces"> Task Scheduler 2.0 Interfaces</a>.

]

The
				<b>NetScheduleJobEnum</b> function lists the jobs queued on a specified computer. This function requires that the schedule service be started.

## -parameters

### -param Servername [in, optional]

A pointer to a constant string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.

### -param PointerToBuffer [out]

A pointer to the buffer that receives the data. The return information is an array of 
<a href="/windows/desktop/api/lmat/ns-lmat-at_enum">AT_ENUM</a> structures. The buffer is allocated by the system and must be freed using a single call to the 
<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a> function. Note that you must free the buffer even if the function fails with ERROR_MORE_DATA.

### -param PrefferedMaximumLength [in]

A value that indicates the preferred maximum length of the returned data, in bytes. If you specify MAX_PREFERRED_LENGTH, the function allocates the amount of memory required for the data. If you specify another value in this parameter, it can restrict the number of bytes that the function returns. If the buffer size is insufficient to hold all entries, the function returns ERROR_MORE_DATA. For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a> and 
<a href="/windows/desktop/NetMgmt/network-management-function-buffer-lengths">Network Management Function Buffer Lengths</a>.

### -param EntriesRead [out]

A pointer to a value that receives the count of elements actually enumerated.

### -param TotalEntries [out]

A pointer to a value that receives the total number of entries that could have been enumerated from the current resume position. Note that applications should consider this value only as a hint.

### -param ResumeHandle [in, out]

A pointer to a value that contains a resume handle which is used to continue a job enumeration. The handle should be zero on the first call and left unchanged for subsequent calls. If this parameter is <b>NULL</b>, then no resume handle is stored.

## -returns

If the function succeeds, the return value is NERR_Success.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

Normally only members of the local Administrators group on the computer where the schedule job is being enumerated can successfully execute this function. If the server name passed in the string pointed to by the <i>Servername</i> parameter is a remote server, then only members of the local Administrators group on the  server can successfully execute this function. 

If the following registry value has the least significant bit set (for example, 0x00000001), then users belonging to the Server Operators group can also successfully execute this function.


<b>HKLM\System\CurrentControlSet\Control\Lsa\SubmitControl</b>

Each entry returned contains an 
<a href="/windows/desktop/api/lmat/ns-lmat-at_enum">AT_ENUM</a> structure. The value of the <b>JobId</b> member can be used when calling functions that require a job identifier parameter, such as the 
<a href="/windows/desktop/api/lmat/nf-lmat-netschedulejobdel">NetScheduleJobDel</a> function.

## -see-also

<a href="/windows/desktop/api/lmat/ns-lmat-at_enum">AT_ENUM</a>



<a href="/windows/desktop/api/lmat/nf-lmat-netschedulejobadd">NetScheduleJobAdd</a>



<a href="/windows/desktop/api/lmat/nf-lmat-netschedulejobdel">NetScheduleJobDel</a>



<a href="/windows/desktop/api/lmat/nf-lmat-netschedulejobgetinfo">NetScheduleJobGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/windows/desktop/NetMgmt/schedule-functions">Schedule
		  Functions</a>