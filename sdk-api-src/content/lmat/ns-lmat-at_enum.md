---
UID: NS:lmat._AT_ENUM
title: AT_ENUM (lmat.h)
description: The AT_ENUM structure contains information about a submitted job. The NetScheduleJobEnum function uses this structure to enumerate and return information about an entire queue of submitted jobs.
helpviewer_keywords: ["*LPAT_ENUM","*PAT_ENUM","AT_ENUM","AT_ENUM structure [Network Management]","JOB_EXEC_ERROR","JOB_NONINTERACTIVE","JOB_RUNS_TODAY","JOB_RUN_PERIODICALLY","LPAT_ENUM","LPAT_ENUM structure pointer [Network Management]","PAT_ENUM","PAT_ENUM structure pointer [Network Management]","_win32_at_enum_str","lmat/AT_ENUM","lmat/LPAT_ENUM","lmat/PAT_ENUM","netmgmt.at_enum_str"]
old-location: netmgmt\at_enum_str.htm
tech.root: NetMgmt
ms.assetid: ed7c5171-b8aa-4a9a-8f31-4d914bcad0b1
ms.date: 12/05/2018
ms.keywords: '*LPAT_ENUM, *PAT_ENUM, AT_ENUM, AT_ENUM structure [Network Management], JOB_EXEC_ERROR, JOB_NONINTERACTIVE, JOB_RUNS_TODAY, JOB_RUN_PERIODICALLY, LPAT_ENUM, LPAT_ENUM structure pointer [Network Management], PAT_ENUM, PAT_ENUM structure pointer [Network Management], _win32_at_enum_str, lmat/AT_ENUM, lmat/LPAT_ENUM, lmat/PAT_ENUM, netmgmt.at_enum_str'
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
req.typenames: AT_ENUM, *PAT_ENUM, *LPAT_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AT_ENUM
 - lmat/_AT_ENUM
 - PAT_ENUM
 - lmat/PAT_ENUM
 - AT_ENUM
 - lmat/AT_ENUM
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
 - AT_ENUM
---

# AT_ENUM structure


## -description

The
				<b>AT_ENUM</b> structure contains information about a submitted job. The 
<a href="/windows/desktop/api/lmat/nf-lmat-netschedulejobenum">NetScheduleJobEnum</a> function uses this structure to enumerate and return information about an entire queue of submitted jobs.

## -struct-fields

### -field JobId

Type: <b>DWORD</b>

The job identifier of a submitted (queued) job.

### -field JobTime

Type: <b>DWORD_PTR</b>

A pointer to the time of day at which the job is scheduled to run. The time is the local time at a computer on which the schedule service is running; it is measured from midnight, and is expressed in milliseconds.

### -field DaysOfMonth

Type: <b>DWORD</b>

A set of bit flags representing the days of the month. For each bit that is set, the scheduled job will run at the time specified by the <b>JobTime</b> member, on the corresponding day of the month. Bit 0 corresponds to the first day of the month, and so on. 




The value of the bitmask is zero if the job was scheduled to run only once, at the first occurrence specified in the <b>JobTime</b> member

### -field DaysOfWeek

Type: <b>UCHAR</b>

A set of bit flags representing the days of the week. For each bit that is set, the scheduled job will run at the time specified by the <b>JobTime</b> member, on the corresponding day of the week. Bit 0 corresponds to Monday, and so on. 




The value of the bitmask is zero if the job was scheduled to run only once, at the first occurrence specified in the <b>JobTime</b> member.

### -field Flags

Type: <b>UCHAR</b>

A set of bit flags describing job properties. This member can be one or more of the following values.

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
This flag is equal to its original value, that is, the value when the job was submitted.

</td>
</tr>
</table>

### -field Command

Type: <b>LPWSTR</b>

A pointer to a Unicode string that contains the name of the command, batch program, or binary file to execute.

## -remarks

For more information about setting the bit flags to schedule jobs that execute once, jobs that execute multiple times, and jobs that execute periodically without deletion, see 
the <a href="/windows/desktop/api/lmat/nf-lmat-netschedulejobadd">NetScheduleJobAdd</a> function.

## -see-also

<a href="/windows/desktop/api/lmat/nf-lmat-netschedulejobenum">NetScheduleJobEnum</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/schedule-functions">Schedule Functions</a>