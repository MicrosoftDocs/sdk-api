---
UID: NF:lmat.NetScheduleJobGetInfo
title: NetScheduleJobGetInfo function (lmat.h)
description: The NetScheduleJobGetInfo function retrieves information about a particular job queued on a specified computer. This function requires that the schedule service be started.
helpviewer_keywords: ["NetScheduleJobGetInfo","NetScheduleJobGetInfo function [Network Management]","_win32_netschedulejobgetinfo","lmat/NetScheduleJobGetInfo","netmgmt.netschedulejobgetinfo"]
old-location: netmgmt\netschedulejobgetinfo.htm
tech.root: NetMgmt
ms.assetid: 44589715-edab-4737-9e49-6f491fd44c28
ms.date: 12/05/2018
ms.keywords: NetScheduleJobGetInfo, NetScheduleJobGetInfo function [Network Management], _win32_netschedulejobgetinfo, lmat/NetScheduleJobGetInfo, netmgmt.netschedulejobgetinfo
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
 - NetScheduleJobGetInfo
 - lmat/NetScheduleJobGetInfo
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
 - NetScheduleJobGetInfo
---

# NetScheduleJobGetInfo function


## -description

<p class="CCE_Message">[<b>NetScheduleJobGetInfo</b> is no longer available for use as of Windows 8. Instead, use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces"> Task Scheduler 2.0 Interfaces</a>.

]

The 
				<b>NetScheduleJobGetInfo</b> function retrieves information about a particular job queued on a specified computer. This function requires that the schedule service be started.

## -parameters

### -param Servername [in, optional]

A pointer to a constant string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.

### -param JobId [in]

A value that indicates the identifier of the job for which to retrieve information.

### -param PointerToBuffer [out]

A pointer to the buffer that receives the 
<a href="/windows/desktop/api/lmat/ns-lmat-at_info">AT_INFO</a> structure describing the specified job. This buffer is allocated by the system and must be freed using the 
<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a> function. For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a> and 
<a href="/windows/desktop/NetMgmt/network-management-function-buffer-lengths">Network Management Function Buffer Lengths</a>.

## -returns

If the function succeeds, the return value is NERR_Success.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

Normally only members of the local Administrators group on the computer where the schedule job is being enumerated can successfully execute this function. If the server name passed in the string pointed to by the <i>Servername</i> parameter is a remote server, then only members of the local Administrators group on the  server can successfully execute this function. 

If the following registry value has the least significant bit set (for example, 0x00000001), then users belonging to the Server Operators group can also successfully execute this function.


<b>HKLM\System\CurrentControlSet\Control\Lsa\SubmitControl</b>

## -see-also

<a href="/windows/desktop/api/lmat/ns-lmat-at_info">AT_INFO</a>



<a href="/windows/desktop/api/lmat/nf-lmat-netschedulejobadd">NetScheduleJobAdd</a>



<a href="/windows/desktop/api/lmat/nf-lmat-netschedulejobdel">NetScheduleJobDel</a>



<a href="/windows/desktop/api/lmat/nf-lmat-netschedulejobenum">NetScheduleJobEnum</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/windows/desktop/NetMgmt/schedule-functions">Schedule
		  Functions</a>