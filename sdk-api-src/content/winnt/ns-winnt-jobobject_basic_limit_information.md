---
UID: NS:winnt._JOBOBJECT_BASIC_LIMIT_INFORMATION
title: JOBOBJECT_BASIC_LIMIT_INFORMATION (winnt.h)
description: Contains basic limit information for a job object.
helpviewer_keywords: ["*PJOBOBJECT_BASIC_LIMIT_INFORMATION","JOBOBJECT_BASIC_LIMIT_INFORMATION","JOBOBJECT_BASIC_LIMIT_INFORMATION structure","JOB_OBJECT_LIMIT_ACTIVE_PROCESS","JOB_OBJECT_LIMIT_AFFINITY","JOB_OBJECT_LIMIT_BREAKAWAY_OK","JOB_OBJECT_LIMIT_DIE_ON_UNHANDLED_EXCEPTION","JOB_OBJECT_LIMIT_JOB_MEMORY","JOB_OBJECT_LIMIT_JOB_TIME","JOB_OBJECT_LIMIT_KILL_ON_JOB_CLOSE","JOB_OBJECT_LIMIT_PRESERVE_JOB_TIME","JOB_OBJECT_LIMIT_PRIORITY_CLASS","JOB_OBJECT_LIMIT_PROCESS_MEMORY","JOB_OBJECT_LIMIT_PROCESS_TIME","JOB_OBJECT_LIMIT_SCHEDULING_CLASS","JOB_OBJECT_LIMIT_SILENT_BREAKAWAY_OK","JOB_OBJECT_LIMIT_SUBSET_AFFINITY","JOB_OBJECT_LIMIT_WORKINGSET","PJOBOBJECT_BASIC_LIMIT_INFORMATION","PJOBOBJECT_BASIC_LIMIT_INFORMATION structure pointer","_JOBOBJECT_BASIC_LIMIT_INFORMATION","_win32_jobobject_basic_limit_information_str","base.jobobject_basic_limit_information_str","winnt/JOBOBJECT_BASIC_LIMIT_INFORMATION","winnt/PJOBOBJECT_BASIC_LIMIT_INFORMATION"]
old-location: base\jobobject_basic_limit_information_str.htm
tech.root: backup
ms.assetid: 83b940a7-05a0-4f5e-bfe3-3f2ac17e2d67
ms.date: 12/05/2018
ms.keywords: '*PJOBOBJECT_BASIC_LIMIT_INFORMATION, JOBOBJECT_BASIC_LIMIT_INFORMATION, JOBOBJECT_BASIC_LIMIT_INFORMATION structure, JOB_OBJECT_LIMIT_ACTIVE_PROCESS, JOB_OBJECT_LIMIT_AFFINITY, JOB_OBJECT_LIMIT_BREAKAWAY_OK, JOB_OBJECT_LIMIT_DIE_ON_UNHANDLED_EXCEPTION, JOB_OBJECT_LIMIT_JOB_MEMORY, JOB_OBJECT_LIMIT_JOB_TIME, JOB_OBJECT_LIMIT_KILL_ON_JOB_CLOSE, JOB_OBJECT_LIMIT_PRESERVE_JOB_TIME, JOB_OBJECT_LIMIT_PRIORITY_CLASS, JOB_OBJECT_LIMIT_PROCESS_MEMORY, JOB_OBJECT_LIMIT_PROCESS_TIME, JOB_OBJECT_LIMIT_SCHEDULING_CLASS, JOB_OBJECT_LIMIT_SILENT_BREAKAWAY_OK, JOB_OBJECT_LIMIT_SUBSET_AFFINITY, JOB_OBJECT_LIMIT_WORKINGSET, PJOBOBJECT_BASIC_LIMIT_INFORMATION, PJOBOBJECT_BASIC_LIMIT_INFORMATION structure pointer, _JOBOBJECT_BASIC_LIMIT_INFORMATION, _win32_jobobject_basic_limit_information_str, base.jobobject_basic_limit_information_str, winnt/JOBOBJECT_BASIC_LIMIT_INFORMATION, winnt/PJOBOBJECT_BASIC_LIMIT_INFORMATION'
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: JOBOBJECT_BASIC_LIMIT_INFORMATION, *PJOBOBJECT_BASIC_LIMIT_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _JOBOBJECT_BASIC_LIMIT_INFORMATION
 - winnt/_JOBOBJECT_BASIC_LIMIT_INFORMATION
 - PJOBOBJECT_BASIC_LIMIT_INFORMATION
 - winnt/PJOBOBJECT_BASIC_LIMIT_INFORMATION
 - JOBOBJECT_BASIC_LIMIT_INFORMATION
 - winnt/JOBOBJECT_BASIC_LIMIT_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - JOBOBJECT_BASIC_LIMIT_INFORMATION
---

# JOBOBJECT_BASIC_LIMIT_INFORMATION structure


## -description

Contains basic limit information for a job object.

## -struct-fields

### -field PerProcessUserTimeLimit

If <b>LimitFlags</b> specifies <b>JOB_OBJECT_LIMIT_PROCESS_TIME</b>, this member is the per-process user-mode execution time limit, in 100-nanosecond ticks. Otherwise, this member is ignored. 




The system periodically checks to determine whether each process associated with the job has accumulated more user-mode time than the set limit. If it has, the process is terminated.

If the job is nested, the effective limit is the most restrictive limit in the job chain.

### -field PerJobUserTimeLimit

If <b>LimitFlags</b> specifies <b>JOB_OBJECT_LIMIT_JOB_TIME</b>, this member is the per-job user-mode execution time limit, in 100-nanosecond ticks. Otherwise, this member is ignored. 




The system adds the current time of the processes associated with the job to this limit. For example, if you set this limit to 1 minute, and the job has a process that has accumulated 5 minutes of user-mode time, the limit actually enforced is 6 minutes.

The system periodically checks to determine whether the sum of the user-mode execution time for all processes is greater than this end-of-job limit. If it is, the action specified in the <b>EndOfJobTimeAction</b> member of the 
<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_end_of_job_time_information">JOBOBJECT_END_OF_JOB_TIME_INFORMATION</a> structure is carried out. By default, all processes are terminated and the status code is set to <b>ERROR_NOT_ENOUGH_QUOTA</b>.

To register  for  notification when this limit is exceeded without terminating processes, use the <a href="/windows/desktop/api/jobapi2/nf-jobapi2-setinformationjobobject">SetInformationJobObject</a> function with the <b>JobObjectNotificationLimitInformation</b> information class.

### -field LimitFlags

The limit flags that are in effect. This member is a bitfield that determines whether other structure members are used. Any combination of the following values can be specified.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMIT_ACTIVE_PROCESS"></a><a id="job_object_limit_active_process"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_ACTIVE_PROCESS</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Establishes a maximum number of simultaneously active processes associated with the job. The <b>ActiveProcessLimit</b> member contains additional information.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMIT_AFFINITY"></a><a id="job_object_limit_affinity"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_AFFINITY</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Causes all processes associated with the job to use the same processor affinity. The <b>Affinity</b> member contains additional information.

If the job is nested, the specified processor affinity must be a subset of the effective affinity of the parent job. If the specified affinity a superset of the affinity of the parent job, it is ignored and the affinity of the parent job is used. 

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMIT_BREAKAWAY_OK"></a><a id="job_object_limit_breakaway_ok"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_BREAKAWAY_OK</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
If any process associated with the job creates a child process using the <b>CREATE_BREAKAWAY_FROM_JOB</b> flag while this limit is in effect, the child process is not associated with the job. 




This limit requires use of a 
<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_extended_limit_information">JOBOBJECT_EXTENDED_LIMIT_INFORMATION</a> structure. Its <b>BasicLimitInformation</b> member  is a 
<b>JOBOBJECT_BASIC_LIMIT_INFORMATION</b> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMIT_DIE_ON_UNHANDLED_EXCEPTION"></a><a id="job_object_limit_die_on_unhandled_exception"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_DIE_ON_UNHANDLED_EXCEPTION</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
Forces a call to the 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode">SetErrorMode</a> function with the <b>SEM_NOGPFAULTERRORBOX</b> flag for each process associated with the job. 




If an exception occurs and the system calls the 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter">UnhandledExceptionFilter</a> function, the debugger will be given a chance to act. If there is no debugger, the functions returns <b>EXCEPTION_EXECUTE_HANDLER</b>. Normally, this will cause termination of the process with the exception code as the exit status.

This limit requires use of a 
<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_extended_limit_information">JOBOBJECT_EXTENDED_LIMIT_INFORMATION</a> structure. Its <b>BasicLimitInformation</b> member is a 
<b>JOBOBJECT_BASIC_LIMIT_INFORMATION</b> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMIT_JOB_MEMORY"></a><a id="job_object_limit_job_memory"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_JOB_MEMORY</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
Causes all processes associated with the job to limit the job-wide sum of their committed memory. When a process attempts to commit memory that would exceed the job-wide limit, it fails. If the job object is associated with a completion port, a <b>JOB_OBJECT_MSG_JOB_MEMORY_LIMIT</b> message is sent to the completion port.

This limit requires use of a 
<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_extended_limit_information">JOBOBJECT_EXTENDED_LIMIT_INFORMATION</a> structure. Its <b>BasicLimitInformation</b> member is a 
<b>JOBOBJECT_BASIC_LIMIT_INFORMATION</b> structure.

To register  for  notification when this limit is exceeded while allowing processes to continue to commit memory, use the <a href="/windows/desktop/api/jobapi2/nf-jobapi2-setinformationjobobject">SetInformationJobObject</a> function with the <b>JobObjectNotificationLimitInformation</b> information class.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMIT_JOB_TIME"></a><a id="job_object_limit_job_time"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_JOB_TIME</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Establishes a user-mode execution time limit for the job. The <b>PerJobUserTimeLimit</b> member contains additional information. This flag cannot be used with <b>JOB_OBJECT_LIMIT_PRESERVE_JOB_TIME</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMIT_KILL_ON_JOB_CLOSE"></a><a id="job_object_limit_kill_on_job_close"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_KILL_ON_JOB_CLOSE</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
Causes all processes associated with the job to terminate when the last handle to the job is closed.

This limit requires use of a 
<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_extended_limit_information">JOBOBJECT_EXTENDED_LIMIT_INFORMATION</a> structure. Its <b>BasicLimitInformation</b> member is a 
<b>JOBOBJECT_BASIC_LIMIT_INFORMATION</b> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMIT_PRESERVE_JOB_TIME"></a><a id="job_object_limit_preserve_job_time"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_PRESERVE_JOB_TIME</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Preserves any job time limits you previously set. As long as this flag is set, you can establish a per-job time limit once, then alter other limits in subsequent calls. This flag cannot be used with <b>JOB_OBJECT_LIMIT_JOB_TIME</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMIT_PRIORITY_CLASS"></a><a id="job_object_limit_priority_class"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_PRIORITY_CLASS</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Causes all processes associated with the job to use the same priority class. For more information, see 
<a href="/windows/desktop/ProcThread/scheduling-priorities">Scheduling Priorities</a>. The <b>PriorityClass</b> member contains additional information.

If the job is nested, the effective priority class is the lowest priority class in the  job chain.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMIT_PROCESS_MEMORY"></a><a id="job_object_limit_process_memory"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_PROCESS_MEMORY</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
Causes all processes associated with the job to limit their committed memory. When a process attempts to commit memory that would exceed the per-process limit, it fails. If the job object is associated with a completion port, a <b>JOB_OBJECT_MSG_PROCESS_MEMORY_LIMIT</b> message is sent to the completion port.

If the job is nested, the effective memory limit is the most restrictive memory limit in the  job chain.

This limit requires use of a 
<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_extended_limit_information">JOBOBJECT_EXTENDED_LIMIT_INFORMATION</a> structure. Its <b>BasicLimitInformation</b> member is a 
<b>JOBOBJECT_BASIC_LIMIT_INFORMATION</b> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMIT_PROCESS_TIME"></a><a id="job_object_limit_process_time"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_PROCESS_TIME</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Establishes a user-mode execution time limit for each currently active process and for all future processes associated with the job. The <b>PerProcessUserTimeLimit</b> member contains additional information.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMIT_SCHEDULING_CLASS"></a><a id="job_object_limit_scheduling_class"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_SCHEDULING_CLASS</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
Causes all processes in the job to use the same scheduling class. The <b>SchedulingClass</b> member contains additional information.

If the job is nested, the effective scheduling class is the lowest scheduling class in the  job chain.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMIT_SILENT_BREAKAWAY_OK"></a><a id="job_object_limit_silent_breakaway_ok"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_SILENT_BREAKAWAY_OK</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
Allows any process associated with the job to create child processes that are not associated with the job. 




If the job is nested and its immediate job object allows breakaway, the child process breaks away from the immediate job object and from each job in the parent job chain, moving up the hierarchy until it reaches a job that does not permit breakaway. If the immediate job object does not allow breakaway, the child process does not break away even if jobs in its parent job chain allow it.

This limit requires use of a 
<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_extended_limit_information">JOBOBJECT_EXTENDED_LIMIT_INFORMATION</a> structure. Its <b>BasicLimitInformation</b> member is a 
<b>JOBOBJECT_BASIC_LIMIT_INFORMATION</b> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMIT_SUBSET_AFFINITY"></a><a id="job_object_limit_subset_affinity"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_SUBSET_AFFINITY</b></dt>
<dt>0x00004000</dt>
</dl>
</td>
<td width="60%">
Allows  processes to use a subset of the  processor affinity for all processes associated with the job. This value must be combined with   <b>JOB_OBJECT_LIMIT_AFFINITY</b>. 

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This flag is supported starting with Windows 7 and Windows Server 2008 R2.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMIT_WORKINGSET"></a><a id="job_object_limit_workingset"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_WORKINGSET</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Causes all processes associated with the job to use the same minimum and maximum working set sizes. The <b>MinimumWorkingSetSize</b> and <b>MaximumWorkingSetSize</b> members contain additional information.

If the job is nested, the effective working set size is the smallest working set size in the  job chain.

</td>
</tr>
</table>

### -field MinimumWorkingSetSize

If <b>LimitFlags</b> specifies <b>JOB_OBJECT_LIMIT_WORKINGSET</b>, this member is the minimum working set size in bytes for each process associated with the job. Otherwise, this member is ignored.

If <b>MaximumWorkingSetSize</b> is nonzero, <b>MinimumWorkingSetSize</b> cannot be zero.

### -field MaximumWorkingSetSize

If <b>LimitFlags</b> specifies <b>JOB_OBJECT_LIMIT_WORKINGSET</b>, this member is the maximum working set size in bytes for each process associated with the job. Otherwise, this member is ignored.

If <b>MinimumWorkingSetSize</b> is nonzero, <b>MaximumWorkingSetSize</b> cannot be zero.

### -field ActiveProcessLimit

If <b>LimitFlags</b> specifies <b>JOB_OBJECT_LIMIT_ACTIVE_PROCESS</b>, this member is the active process limit for the job. Otherwise, this member is ignored.

If you try to associate a process with a job, and this causes the active process count to exceed this limit, the process is terminated and the association fails.

### -field Affinity

If <b>LimitFlags</b> specifies <b>JOB_OBJECT_LIMIT_AFFINITY</b>, this member is the processor affinity for all processes associated with the job. Otherwise, this member is ignored.

The affinity must be a subset of the system affinity mask obtained by calling the 
<a href="/windows/desktop/api/winbase/nf-winbase-getprocessaffinitymask">GetProcessAffinityMask</a> function. The affinity of each thread is set to this value, but threads are free to subsequently set their affinity, as long as it is a subset of the specified affinity mask. Processes cannot set their own affinity mask.

### -field PriorityClass

If <b>LimitFlags</b> specifies <b>JOB_OBJECT_LIMIT_PRIORITY_CLASS</b>, this member is the priority class for all processes associated with the job. Otherwise, this member is ignored.

Processes and threads cannot modify their priority class. The calling process must enable the <b>SE_INC_BASE_PRIORITY_NAME</b> privilege.

### -field SchedulingClass

If <b>LimitFlags</b> specifies <b>JOB_OBJECT_LIMIT_SCHEDULING_CLASS</b>, this member is the scheduling class for all processes associated with the job. Otherwise, this member is ignored.

The valid values are 0 to 9. Use 0 for the least favorable scheduling class relative to other threads, and 9 for the most favorable scheduling class relative to other threads. By default, this value is 5. To use a scheduling class greater than 5, the calling process must enable the <b>SE_INC_BASE_PRIORITY_NAME</b> privilege.

## -remarks

Processes can still empty their working sets using the 
<a href="/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsize">SetProcessWorkingSetSize</a> function with (<b>SIZE_T</b>)-1, even when <b>JOB_OBJECT_LIMIT_WORKINGSET</b> is used. However, you cannot use <b>SetProcessWorkingSetSize</b> change the minimum or maximum working set size of a process in a job object.

The system increments the active process count when you attempt to associate a process with a job. If the limit is exceeded, the system decrements the active process count only when the process terminates and all handles to the process are closed. Therefore, if you have an open handle to a process that has been terminated in such a manner, you cannot associate any new processes until the handle is closed and the active process count is below the limit.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-getprocessaffinitymask">GetProcessAffinityMask</a>



<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_end_of_job_time_information">JOBOBJECT_END_OF_JOB_TIME_INFORMATION</a>



<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_extended_limit_information">JOBOBJECT_EXTENDED_LIMIT_INFORMATION</a>



<a href="/windows/win32/api/winnt/ns-winnt-jobobject_notification_limit_information">JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION</a>



<a href="/windows/desktop/api/jobapi2/nf-jobapi2-queryinformationjobobject">QueryInformationJobObject</a>



<a href="/windows/desktop/api/jobapi2/nf-jobapi2-setinformationjobobject">SetInformationJobObject</a>



<a href="/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsize">SetProcessWorkingSetSize</a>