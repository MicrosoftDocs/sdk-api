---
UID: NS:winnt._JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION
title: JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION (winnt.h)
description: Contains information about notification limits for a job object. This structure is used by the SetInformationJobObject and QueryInformationJobObject functions with the JobObjectNotificationLimitInformation information class.
helpviewer_keywords: ["*PJOBOBJECT_NOTIFICATION_LIMIT_INFORMATION","JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION","JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION structure","JOB_OBJECT_LIMIT_JOB_MEMORY","JOB_OBJECT_LIMIT_JOB_READ_BYTES","JOB_OBJECT_LIMIT_JOB_TIME","JOB_OBJECT_LIMIT_JOB_WRITE_BYTES","JOB_OBJECT_LIMIT_RATE_CONTROL","PJOBOBJECT_NOTIFICATION_LIMIT_INFORMATION","PJOBOBJECT_NOTIFICATION_LIMIT_INFORMATION structure pointer","ToleranceHigh","ToleranceIntervalLong","ToleranceIntervalMedium","ToleranceIntervalShort","ToleranceLow","ToleranceMedium","_JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION","base.jobobject_notification_limit_information","winnt/JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION","winnt/PJOBOBJECT_NOTIFICATION_LIMIT_INFORMATION"]
old-location: base\jobobject_notification_limit_information.htm
tech.root: backup
ms.assetid: 39cf5f26-dfc1-4f1d-aae4-5f29e277834f
ms.date: 12/05/2018
ms.keywords: '*PJOBOBJECT_NOTIFICATION_LIMIT_INFORMATION, JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION, JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION structure, JOB_OBJECT_LIMIT_JOB_MEMORY, JOB_OBJECT_LIMIT_JOB_READ_BYTES, JOB_OBJECT_LIMIT_JOB_TIME, JOB_OBJECT_LIMIT_JOB_WRITE_BYTES, JOB_OBJECT_LIMIT_RATE_CONTROL, PJOBOBJECT_NOTIFICATION_LIMIT_INFORMATION, PJOBOBJECT_NOTIFICATION_LIMIT_INFORMATION structure pointer, ToleranceHigh, ToleranceIntervalLong, ToleranceIntervalMedium, ToleranceIntervalShort, ToleranceLow, ToleranceMedium, _JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION, base.jobobject_notification_limit_information, winnt/JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION, winnt/PJOBOBJECT_NOTIFICATION_LIMIT_INFORMATION'
req.header: winnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION, *PJOBOBJECT_NOTIFICATION_LIMIT_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION
 - winnt/_JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION
 - PJOBOBJECT_NOTIFICATION_LIMIT_INFORMATION
 - winnt/PJOBOBJECT_NOTIFICATION_LIMIT_INFORMATION
 - JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION
 - winnt/JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION
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
 - JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION
---

# JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION structure


## -description

Contains information about notification limits for a job object. This structure is used by the <a href="/windows/desktop/api/jobapi2/nf-jobapi2-setinformationjobobject">SetInformationJobObject</a> and <a href="/windows/desktop/api/jobapi2/nf-jobapi2-queryinformationjobobject">QueryInformationJobObject</a> functions with the <b>JobObjectNotificationLimitInformation</b> information class.

## -struct-fields

### -field IoReadBytesLimit

If the <i>LimitFlags</i> member specifies JOB_OBJECT_LIMIT_JOB_READ_BYTES, this member is the notification limit for total I/O bytes read by all processes in the job. Otherwise, this member is ignored.

### -field IoWriteBytesLimit

If the <i>LimitFlags</i> parameter specifies JOB_OBJECT_LIMIT_JOB_WRITE_BYTES, this member is the notification limit for total I/O bytes written by all processes in the job. Otherwise, this member is ignored.

### -field PerJobUserTimeLimit

If the <i>LimitFlags</i> parameter specifies JOB_OBJECT_LIMIT_JOB_TIME, this member is the notification limit for per-job user-mode execution time, in 100-nanosecond ticks. Otherwise, this member is ignored.

The system adds the accumulated execution time of processes associated with the job to this limit when the limit is set. For example, if a process associated with the job has already accumulated 5 minutes of user-mode execution time and the limit is set to 1 minute, the limit actually enforced is 6 minutes.

To specify <b>PerJobUserTimeLimit</b> as an enforceable limit and terminate processes in jobs that exceed the limit, see the <a href="/windows/desktop/api/winnt/ns-winnt-jobobject_basic_limit_information">JOBOBJECT_BASIC_LIMIT_INFORMATION</a> structure.

### -field JobMemoryLimit

If the <i>LimitFlags</i> parameter specifies JOB_OBJECT_LIMIT_JOB_MEMORY, this member is the notification limit for total virtual memory that can be committed by all processes in the job, in bytes. Otherwise, this member is ignored.

To specify <b>JobMemoryLimit</b> as an enforceable limit and prevent processes in jobs that exceed the limit from continuing to commit memory, see the <a href="/windows/desktop/api/winnt/ns-winnt-jobobject_basic_limit_information">JOBOBJECT_EXTENDED_LIMIT_INFORMATION</a> structure.

### -field RateControlTolerance

If the <i>LimitFlags</i> parameter specifies JOB_OBJECT_LIMIT_RATE_CONTROL, this member specifies the extent to which a job can exceed its CPU rate control limits during the interval specified by the <b>RateControlToleranceInterval</b> member.  Otherwise, this member is ignored. 

This member can be one of the following values. If no value is specified, <b>ToleranceHigh</b> is used.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ToleranceLow"></a><a id="tolerancelow"></a><a id="TOLERANCELOW"></a><dl>
<dt><b>ToleranceLow</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The job can exceed its CPU rate control limits for 20% of the tolerance interval.

</td>
</tr>
<tr>
<td width="40%"><a id="ToleranceMedium"></a><a id="tolerancemedium"></a><a id="TOLERANCEMEDIUM"></a><dl>
<dt><b>ToleranceMedium</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The job can exceed its CPU rate control limits for 40% of the tolerance interval.

</td>
</tr>
<tr>
<td width="40%"><a id="ToleranceHigh"></a><a id="tolerancehigh"></a><a id="TOLERANCEHIGH"></a><dl>
<dt><b>ToleranceHigh</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The job can exceed its CPU rate control limits for 60% of the tolerance interval.

</td>
</tr>
</table>

### -field RateControlToleranceInterval

If the <i>LimitFlags</i> parameter specifies JOB_OBJECT_LIMIT_RATE_CONTROL, this member specifies the interval during which a job's CPU usage is monitored to determine whether the job has exceeded its CPU rate control limits. Otherwise, this member is ignored. 

This member can be one of the following values. If no value is specified, <b>ToleranceIntervalShort</b> is used.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ToleranceIntervalShort"></a><a id="toleranceintervalshort"></a><a id="TOLERANCEINTERVALSHORT"></a><dl>
<dt><b>ToleranceIntervalShort</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The tolerance interval is 10 seconds. 

</td>
</tr>
<tr>
<td width="40%"><a id="ToleranceIntervalMedium"></a><a id="toleranceintervalmedium"></a><a id="TOLERANCEINTERVALMEDIUM"></a><dl>
<dt><b>ToleranceIntervalMedium</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The tolerance interval is one minute. 

</td>
</tr>
<tr>
<td width="40%"><a id="ToleranceIntervalLong"></a><a id="toleranceintervallong"></a><a id="TOLERANCEINTERVALLONG"></a><dl>
<dt><b>ToleranceIntervalLong</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The tolerance interval is 10 minutes. 

</td>
</tr>
</table>

### -field LimitFlags

The limit flags that are in effect. This member is a bitfield that determines whether other structure members are used. Any combination of the following values can be specified.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMIT_JOB_MEMORY"></a><a id="job_object_limit_job_memory"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_JOB_MEMORY</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
Establishes the committed memory  limit to the job-wide sum of committed memory for all processes associated with the job. The <b>JobMemoryLimit</b> member contains additional information.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMIT_JOB_READ_BYTES"></a><a id="job_object_limit_job_read_bytes"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_JOB_READ_BYTES</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
Establishes the I/O read bytes limit to the job-wide sum of I/O bytes read by all processes associated with the job. The <b>IoReadBytesLimit</b> member contains more information.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMIT_JOB_WRITE_BYTES"></a><a id="job_object_limit_job_write_bytes"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_JOB_WRITE_BYTES</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
Establishes the I/O write bytes limit to the job-wide sum of  I/O bytes written by all processes associated with the job. The <b>IoWriteBytesLimit</b> member contains more information.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMIT_JOB_TIME"></a><a id="job_object_limit_job_time"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_JOB_TIME</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Establishes the limit for user-mode execution time for the job. The <b>PerJobUserTimeLimit</b> member contains additional information. 

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMIT_RATE_CONTROL"></a><a id="job_object_limit_rate_control"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_RATE_CONTROL</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
Establishes the notification threshold for the CPU rate control limits established for the job. The <b>RateControlTolerance</b> and <b>RateControlToleranceInterval</b> members contain additional information.

CPU rate control limits are established by calling <a href="/windows/desktop/api/jobapi2/nf-jobapi2-setinformationjobobject">SetInformationJobObject</a> with the <b>JobObjectCpuRateInformationClass</b> information class. 

</td>
</tr>
</table>

## -remarks

When a notification limit is exceeded, the system sends a JOB_OBJECT_MSG_NOTIFICATION_LIMIT message to the I/O completion port associated with the job. Processes in the job continue to run and can continue to allocate memory or transmit read or write bytes beyond the specified limits. 

When the application monitoring the I/O completion port receives a JOB_OBJECT_MSG_NOTIFICATION_LIMIT message, it must call <a href="/windows/desktop/api/jobapi2/nf-jobapi2-queryinformationjobobject">QueryInformationJobObject</a> with the <b>JobObjectLimitViolationInformation</b> information class. Limit violation information is received in a JOBOBJECT_LIMIT_VIOLATION_STRUCTURE that contains information about all notification limits that were exceeded at the time of the query. The system will not send another JOB_OBJECT_MSG_NOTIFICATION_LIMIT message until after   <b>QueryInformationJobObject</b> is called.  

CPU rate control limits for a job are established in a <a href="/windows/desktop/api/winnt/ns-winnt-jobobject_cpu_rate_control_information">JOBOBJECT_CPU_RATE_CONTROL_INFORMATION</a> structure. The CPU rate control values in the <b>JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION</b> structure specify how much the job can exceed its established CPU rate control limits before notification is sent.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_cpu_rate_control_information">JOBOBJECT_CPU_RATE_CONTROL_INFORMATION</a>



<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_limit_violation_information">JOBOBJECT_LIMIT_VIOLATION_INFORMATION</a>



<a href="/windows/desktop/api/jobapi2/nf-jobapi2-queryinformationjobobject">QueryInformationJobObject</a>



<a href="/windows/desktop/api/jobapi2/nf-jobapi2-setinformationjobobject">SetInformationJobObject</a>