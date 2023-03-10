---
UID: NF:lmat.NetScheduleJobDel
title: NetScheduleJobDel function (lmat.h)
description: The NetScheduleJobDel function deletes a range of jobs queued to run at a computer. This function requires that the schedule service be started at the computer to which the job deletion request is being sent.
helpviewer_keywords: ["NetScheduleJobDel","NetScheduleJobDel function [Network Management]","_win32_netschedulejobdel","lmat/NetScheduleJobDel","netmgmt.netschedulejobdel"]
old-location: netmgmt\netschedulejobdel.htm
tech.root: NetMgmt
ms.assetid: 5ae668ab-f51d-457e-a239-2ec16a0e5a55
ms.date: 12/05/2018
ms.keywords: NetScheduleJobDel, NetScheduleJobDel function [Network Management], _win32_netschedulejobdel, lmat/NetScheduleJobDel, netmgmt.netschedulejobdel
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
 - NetScheduleJobDel
 - lmat/NetScheduleJobDel
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
 - NetScheduleJobDel
---

# NetScheduleJobDel function


## -description

<p class="CCE_Message">[<b>NetScheduleJobDel</b> is no longer available for use as of Windows 8. Instead, use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces"> Task Scheduler 2.0 Interfaces</a>.

]

The
				<b>NetScheduleJobDel</b> function deletes a range of jobs queued to run at a computer. This function requires that the schedule service be started at the computer to which the job deletion request is being sent.

## -parameters

### -param Servername [in, optional]

A pointer to a constant string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.

### -param MinJobId [in]

The minimum job identifier. Jobs with a job identifier smaller than <i>MinJobId</i> will not be deleted.

### -param MaxJobId [in]

The  maximum job identifier. Jobs with a job identifier larger than <i>MaxJobId</i> will not be deleted.

## -returns

If the function succeeds, the return value is NERR_Success.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

Normally only members of the local Administrators group on the computer where the schedule job is being deleted can successfully execute this function. If the server name passed in the string pointed to by the <i>Servername</i> parameter is a remote server, then only members of the local Administrators group on the  server can successfully execute this function. 

If the following registry value has the least significant bit set (for example, 0x00000001), then users belonging to the Server Operators group can also successfully execute this function.


<b>HKLM\System\CurrentControlSet\Control\Lsa\SubmitControl</b>

Call the 
<a href="/windows/desktop/api/lmat/nf-lmat-netschedulejobenum">NetScheduleJobEnum</a> function to retrieve the job identifier for one or more scheduled jobs.

The 
<b>NetScheduleJobDel</b> function deletes all jobs whose job identifiers are in the range <i>MinJobId</i> through <i>MaxJobId</i>.

To delete all scheduled jobs at the server, you can call 
<b>NetScheduleJobDel</b> specifying <i>MinJobId</i> equal to 0 and <i>MaxJobId</i> equal to – 1. To delete one job, specify the job's identifier for both the <i>MinJobId</i> parameter and the <i>MaxJobId</i> parameter.

## -see-also

<a href="/windows/desktop/api/lmat/nf-lmat-netschedulejobadd">NetScheduleJobAdd</a>



<a href="/windows/desktop/api/lmat/nf-lmat-netschedulejobenum">NetScheduleJobEnum</a>



<a href="/windows/desktop/api/lmat/nf-lmat-netschedulejobgetinfo">NetScheduleJobGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/windows/desktop/NetMgmt/schedule-functions">Schedule
		  Functions</a>