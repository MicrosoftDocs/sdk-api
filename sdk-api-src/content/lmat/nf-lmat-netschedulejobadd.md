---
UID: NF:lmat.NetScheduleJobAdd
title: NetScheduleJobAdd function (lmat.h)
description: The NetScheduleJobAdd function submits a job to run at a specified future time and date. This function requires that the schedule service be started on the computer to which the job is submitted.
helpviewer_keywords: ["NetScheduleJobAdd","NetScheduleJobAdd function [Network Management]","_win32_netschedulejobadd","lmat/NetScheduleJobAdd","netmgmt.netschedulejobadd"]
old-location: netmgmt\netschedulejobadd.htm
tech.root: NetMgmt
ms.assetid: 813d13ba-abe1-4b14-88c7-87ba88a42a3b
ms.date: 12/05/2018
ms.keywords: NetScheduleJobAdd, NetScheduleJobAdd function [Network Management], _win32_netschedulejobadd, lmat/NetScheduleJobAdd, netmgmt.netschedulejobadd
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
 - NetScheduleJobAdd
 - lmat/NetScheduleJobAdd
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
 - NetScheduleJobAdd
---

# NetScheduleJobAdd function


## -description

<p class="CCE_Message">[<b>NetScheduleJobAdd</b> is no longer available for use as of Windows 8. Instead, use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces"> Task Scheduler 2.0 Interfaces</a>.

]

The
				<b>NetScheduleJobAdd</b> function submits a job to run at a specified future time and date. This function requires that the schedule service be started on  the computer to which the job is submitted.

## -parameters

### -param Servername [in, optional]

A pointer to a constant string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.

### -param Buffer [in]

A pointer to an 
<a href="/windows/desktop/api/lmat/ns-lmat-at_info">AT_INFO</a> structure describing the job to submit. For more information about scheduling jobs using different job properties, see the following Remarks section and 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a>.

### -param JobId [out]

A pointer that receives a job identifier for the newly submitted job. This entry is valid only if the function returns successfully.

## -returns

If the function succeeds, the return value is NERR_Success.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

Normally only members of the local Administrators group on the computer where the schedule job is being added can successfully execute this function. If the server name passed in the string pointed to by the <i>Servername</i> parameter is a remote server, then only members of the local Administrators group on the  remote server can successfully execute this function. 

If the following registry value has the least significant bit set (for example, 0x00000001), then users belonging to the Server Operators group can also successfully execute this function.


<b>HKLM\System\CurrentControlSet\Control\Lsa\SubmitControl</b>

The following are examples of how to schedule jobs using different properties supported by the 
<b>NetScheduleJobAdd</b> function.

To schedule a job that executes once:

<ul>
<li>Set the <b>DaysOfMonth</b> member of the 
<a href="/windows/desktop/api/lmat/ns-lmat-at_info">AT_INFO</a> structure to zero.</li>
<li>Set the <b>DaysOfWeek</b> member of the 
<a href="/windows/desktop/api/lmat/ns-lmat-at_info">AT_INFO</a> structure to zero.</li>
<li>Set the <b>JobTime</b> member of the 
<a href="/windows/desktop/api/lmat/ns-lmat-at_info">AT_INFO</a> structure to the time the job should execute.</li>
</ul>
The job executes at the time specified by the <b>JobTime</b> member of the 
<a href="/windows/desktop/api/lmat/ns-lmat-at_info">AT_INFO</a> structure pointed to by the <i>Buffer</i> parameter. After the job executes, it is deleted.

To schedule and delete a job that executes multiple times:

<ul>
<li>Set the appropriate bits in the  <b>DaysOfMonth</b> member of the 
<a href="/windows/desktop/api/lmat/ns-lmat-at_info">AT_INFO</a> structure or </li>
<li>Set the appropriate bits in the  <b>DaysOfWeek</b> member of the 
<a href="/windows/desktop/api/lmat/ns-lmat-at_info">AT_INFO</a> structure. </li>
<li>Set the <b>JobTime</b> member of the 
<a href="/windows/desktop/api/lmat/ns-lmat-at_info">AT_INFO</a> structure to the time the job should execute.</li>
</ul>
<div class="alert"><b>Note</b>  You do not need to set both the  <b>DaysOfMonth</b> and the  <b>DaysOfWeek</b> members of the 
<a href="/windows/desktop/api/lmat/ns-lmat-at_info">AT_INFO</a> structure.</div>
<div> </div>
The job executes at the time specified by the <b>JobTime</b> member of the 
<a href="/windows/desktop/api/lmat/ns-lmat-at_info">AT_INFO</a> structure pointed to by the <i>Buffer</i> parameter, once for each day set in the  <b>DaysOfMonth</b> or <b>DaysOfWeek</b> members of the 
<a href="/windows/desktop/api/lmat/ns-lmat-at_info">AT_INFO</a> structure. After each job executes, the corresponding bit is cleared. When the last bit is cleared, the job is deleted.

To schedule a job that executes periodically:

<ul>
<li>Set the appropriate bits in the <b>DaysOfMonth</b> member of the 
<a href="/windows/desktop/api/lmat/ns-lmat-at_info">AT_INFO</a> structure or</li>
<li>Set the appropriate bits in the <b>DaysOfWeek</b> member of the 
<a href="/windows/desktop/api/lmat/ns-lmat-at_info">AT_INFO</a> structure. </li>
<li>Set the <b>JobTime</b> member of the 
<a href="/windows/desktop/api/lmat/ns-lmat-at_info">AT_INFO</a> structure to the time the job should execute.</li>
<li>Set the job submission flag JOB_RUN_PERIODICALLY in the <b>Flags</b> member of the 
<a href="/windows/desktop/api/lmat/ns-lmat-at_info">AT_INFO</a> structure.</li>
</ul>
<div class="alert"><b>Note</b>  You do not need to set both the  <b>DaysOfMonth</b> and the  <b>DaysOfWeek</b> members of the 
<a href="/windows/desktop/api/lmat/ns-lmat-at_info">AT_INFO</a> structure.</div>
<div> </div>
The job will execute periodically, at the time specified by the <b>JobTime</b> member of the 
<a href="/windows/desktop/api/lmat/ns-lmat-at_info">AT_INFO</a> structure pointed to by the <i>Buffer</i> parameter, on each day set in the <b>DaysOfMonth</b> or <b>DaysOfWeek</b> member of the 
<a href="/windows/desktop/api/lmat/ns-lmat-at_info">AT_INFO</a> structure. The job will not be deleted as a result of the repeated executions. The only way to delete the job is by an explicit call to the 
<a href="/windows/desktop/api/lmat/nf-lmat-netschedulejobdel">NetScheduleJobDel</a> function.

See 
the <a href="/windows/desktop/api/lmat/ns-lmat-at_info">AT_INFO</a> structure for a description of the <b>DaysOfWeek</b>, <b>DaysOfMonth</b>, and  job property bitmasks.

On Windows 2000, the earlier AT service and the Task Scheduler were combined. The Task Scheduler service was only accurate to the minute.  Therefore, the <b>NetScheduleJobAdd</b> function only uses hours and minutes specified in the <b>JobTime</b> member of the <a href="/windows/desktop/api/lmat/ns-lmat-at_info">AT_INFO</a> structure when a job is scheduled to run. 

Starting with   Windows Vista, the precision for the Task Scheduler was increased to the second. Therefore, the <b>NetScheduleJobAdd</b> function uses only the hours, minutes, and seconds specified in the <b>JobTime</b> member of the <a href="/windows/desktop/api/lmat/ns-lmat-at_info">AT_INFO</a> structure when a job is scheduled to run.

## -see-also

<a href="/windows/desktop/api/lmat/ns-lmat-at_info">AT_INFO</a>



<a href="/windows/desktop/api/lmat/nf-lmat-netschedulejobdel">NetScheduleJobDel</a>



<a href="/windows/desktop/api/lmat/nf-lmat-netschedulejobenum">NetScheduleJobEnum</a>



<a href="/windows/desktop/api/lmat/nf-lmat-netschedulejobgetinfo">NetScheduleJobGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/windows/desktop/NetMgmt/schedule-functions">Schedule
		  Functions</a>