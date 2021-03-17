---
UID: NS:lmat._AT_INFO
title: AT_INFO (lmat.h)
description: The AT_INFO structure contains information about a job.
helpviewer_keywords: ["*LPAT_INFO","*PAT_INFO","AT_INFO","AT_INFO structure [Network Management]","JOB_ADD_CURRENT_DATE","JOB_EXEC_ERROR","JOB_NONINTERACTIVE","JOB_RUNS_TODAY","JOB_RUN_PERIODICALLY","LPAT_INFO","LPAT_INFO structure pointer [Network Management]","PAT_INFO","PAT_INFO structure pointer [Network Management]","_win32_at_info_str","lmat/AT_INFO","lmat/LPAT_INFO","lmat/PAT_INFO","netmgmt.at_info_str"]
old-location: netmgmt\at_info_str.htm
tech.root: NetMgmt
ms.assetid: eb0bf696-53ca-432a-b04c-5e0b6a61a0fd
ms.date: 12/05/2018
ms.keywords: '*LPAT_INFO, *PAT_INFO, AT_INFO, AT_INFO structure [Network Management], JOB_ADD_CURRENT_DATE, JOB_EXEC_ERROR, JOB_NONINTERACTIVE, JOB_RUNS_TODAY, JOB_RUN_PERIODICALLY, LPAT_INFO, LPAT_INFO structure pointer [Network Management], PAT_INFO, PAT_INFO structure pointer [Network Management], _win32_at_info_str, lmat/AT_INFO, lmat/LPAT_INFO, lmat/PAT_INFO, netmgmt.at_info_str'
req.header: lmat.h
req.include-header: Lm.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: AT_INFO, *PAT_INFO, *LPAT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AT_INFO
 - lmat/_AT_INFO
 - PAT_INFO
 - lmat/PAT_INFO
 - AT_INFO
 - lmat/AT_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmat.h
api_name:
 - AT_INFO
---

# AT_INFO structure


## -description

The
				<b>AT_INFO</b> structure contains information about a job. The 
<a href="/windows/desktop/api/lmat/nf-lmat-netschedulejobadd">NetScheduleJobAdd</a> function uses the structure to specify information when scheduling a job. The 
<a href="/windows/desktop/api/lmat/nf-lmat-netschedulejobgetinfo">NetScheduleJobGetInfo</a> function uses the structure to retrieve information about a job that has already been submitted.

## -struct-fields

### -field JobTime

Type: <b>DWORD_PTR</b>

A pointer to a value that indicates the time of day at which the job is scheduled to run. The time is the local time at a computer on which the schedule service is running; it is measured from midnight, and is expressed in milliseconds.

### -field DaysOfMonth

Type: <b>DWORD</b>

A set of bit flags representing the days of the month. For each bit that is set, the scheduled job will run at the time specified by the <b>JobTime</b> member, on the corresponding day of the month. Bit 0 corresponds to the first day of the month, and so on.

The value of the bitmask is zero if the job was scheduled to run only once, at the first occurrence specified by the <b>JobTime</b> member.

### -field DaysOfWeek

Type: <b>UCHAR</b>

A set of bit flags representing the days of the week. For each bit that is set, the scheduled job will run at the time specified by the <b>JobTime</b> member, on the corresponding day of the week. Bit 0 corresponds to Monday, and so on. 




The value of the bitmask is zero if the job was scheduled to run only once, at the first occurrence specified by the <b>JobTime</b> member.

### -field Flags

Type: <b>UCHAR</b>

A set of bit flags describing job properties. 




 When you submit a job using a call to the 
<a href="/windows/desktop/api/lmat/nf-lmat-netschedulejobadd">NetScheduleJobAdd</a> function, you can specify one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="JOB_RUN_PERIODICALLY"></a><a id="job_run_periodically"></a><dl>
<dt><b>JOB_RUN_PERIODICALLY</b></dt>
</dl>
</td>
<td width="60%">
If you set this flag, the job runs, and continues to run, on each day for which a corresponding bit is set in the <b>DaysOfMonth</b> member or the <b>DaysOfWeek</b> member. The job is not deleted after it executes. 




If this flag is clear, the job runs only once for each bit set in these members. The job is deleted after it executes once.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_ADD_CURRENT_DATE"></a><a id="job_add_current_date"></a><dl>
<dt><b>JOB_ADD_CURRENT_DATE</b></dt>
</dl>
</td>
<td width="60%">
If you set this flag, the job executes at the first occurrence of <b>JobTime</b> member at the computer where the job is queued. 




Setting this flag is equivalent to setting the bit for the current day in the <b>DaysOfMonth</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_NONINTERACTIVE"></a><a id="job_noninteractive"></a><dl>
<dt><b>JOB_NONINTERACTIVE</b></dt>
</dl>
</td>
<td width="60%">
If you set this flag, the job does not run interactively. 




If this flag is clear, the job runs interactively.

</td>
</tr>
</table>
 

 When you call 
<a href="/windows/desktop/api/lmat/nf-lmat-netschedulejobgetinfo">NetScheduleJobGetInfo</a> to retrieve job information, the function can return one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="JOB_RUN_PERIODICALLY"></a><a id="job_run_periodically"></a><dl>
<dt><b>JOB_RUN_PERIODICALLY</b></dt>
</dl>
</td>
<td width="60%">
This flag is equal to its original value, that is, the value when the job was submitted.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_EXEC_ERROR"></a><a id="job_exec_error"></a><dl>
<dt><b>JOB_EXEC_ERROR</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, it indicates that the schedule service failed to successfully execute the job the last time it was scheduled to run.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_RUNS_TODAY"></a><a id="job_runs_today"></a><dl>
<dt><b>JOB_RUNS_TODAY</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, it indicates that the job is scheduled to execute on the current day; the value of the <b>JobTime</b> member is greater than the current time of day at the computer where the job is queued.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_NONINTERACTIVE"></a><a id="job_noninteractive"></a><dl>
<dt><b>JOB_NONINTERACTIVE</b></dt>
</dl>
</td>
<td width="60%">
This flag bit is equal to its original value, that is, the value when the job was submitted.

</td>
</tr>
</table>

### -field Command

Type: <b>LPWSTR</b>

A pointer to a Unicode string that contains the name of the command, batch program, or binary file to execute.

## -remarks

For more information about scheduling jobs that execute once, jobs that execute multiple times, and jobs that execute periodically without deletion, see 
<a href="/windows/desktop/api/lmat/nf-lmat-netschedulejobadd">NetScheduleJobAdd</a>.

## -see-also

<a href="/windows/desktop/api/lmat/nf-lmat-netschedulejobadd">NetScheduleJobAdd</a>



<a href="/windows/desktop/api/lmat/nf-lmat-netschedulejobgetinfo">NetScheduleJobGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/schedule-functions">Schedule Functions</a>