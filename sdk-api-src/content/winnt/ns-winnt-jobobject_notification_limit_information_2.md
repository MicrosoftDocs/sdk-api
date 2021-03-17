---
UID: NS:winnt.JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION_2
title: JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION_2 (winnt.h)
description: Contains extended information about notification limits for a job object. This structure is used by the SetInformationJobObject and QueryInformationJobObject functions with the JobObjectNotificationLimitInformation2 information class.
helpviewer_keywords: ["JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION_2","JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION_2 structure","JOB_OBJECT_LIMIT_CPU_RATE_CONTROL","JOB_OBJECT_LIMIT_IO_RATE_CONTROL","JOB_OBJECT_LIMIT_JOB_MEMORY_HIGH","JOB_OBJECT_LIMIT_JOB_MEMORY_LOW","JOB_OBJECT_LIMIT_JOB_READ_BYTES","JOB_OBJECT_LIMIT_JOB_TIME","JOB_OBJECT_LIMIT_JOB_WRITE_BYTES","JOB_OBJECT_LIMIT_NET_RATE_CONTROL","JOB_OBJECT_LIMIT_RATE_CONTROL","ToleranceHigh","ToleranceIntervalLong","ToleranceIntervalMedium","ToleranceIntervalShort","ToleranceLow","ToleranceMedium","base.jobobject_notification_limit_information_2","winnt/JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION_2"]
old-location: base\jobobject_notification_limit_information_2.htm
tech.root: backup
ms.assetid: AFF8986F-6BC7-4683-99AC-EC82FFA27339
ms.date: 12/05/2018
ms.keywords: JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION_2, JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION_2 structure, JOB_OBJECT_LIMIT_CPU_RATE_CONTROL, JOB_OBJECT_LIMIT_IO_RATE_CONTROL, JOB_OBJECT_LIMIT_JOB_MEMORY_HIGH, JOB_OBJECT_LIMIT_JOB_MEMORY_LOW, JOB_OBJECT_LIMIT_JOB_READ_BYTES, JOB_OBJECT_LIMIT_JOB_TIME, JOB_OBJECT_LIMIT_JOB_WRITE_BYTES, JOB_OBJECT_LIMIT_NET_RATE_CONTROL, JOB_OBJECT_LIMIT_RATE_CONTROL, ToleranceHigh, ToleranceIntervalLong, ToleranceIntervalMedium, ToleranceIntervalShort, ToleranceLow, ToleranceMedium, base.jobobject_notification_limit_information_2, winnt/JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION_2
req.header: winnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION_2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION_2
 - winnt/JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION_2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION_2
---

# JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION_2 structure


## -description

Contains extended information about notification limits for a job object. This structure is used by the <a href="/windows/desktop/api/jobapi2/nf-jobapi2-setinformationjobobject">SetInformationJobObject</a> and <a href="/windows/desktop/api/jobapi2/nf-jobapi2-queryinformationjobobject">QueryInformationJobObject</a> functions with the <b>JobObjectNotificationLimitInformation2</b> information class.

## -struct-fields

### -field IoReadBytesLimit

If the <i>LimitFlags</i> member specifies <b>JOB_OBJECT_LIMIT_JOB_READ_BYTES</b>, this member is the notification limit for the total I/O bytes read by all processes in the job. Otherwise, this member is ignored.

### -field IoWriteBytesLimit

If the <i>LimitFlags</i> parameter specifies <b>JOB_OBJECT_LIMIT_JOB_WRITE_BYTES</b>, this member is the notification limit for the total I/O bytes written by all processes in the job. Otherwise, this member is ignored.

### -field PerJobUserTimeLimit

If the <i>LimitFlags</i> parameter specifies <b>JOB_OBJECT_LIMIT_JOB_TIME</b>, this member is the notification limit for per-job user-mode execution time, in 100-nanosecond ticks. Otherwise, this member is ignored.

The system adds the accumulated execution time of processes associated with the job to this limit when the limit is set. For example, if a process associated with the job has already accumulated 5 minutes of user-mode execution time and the limit is set to 1 minute, the limit actually enforced is 6 minutes.

To specify <b>PerJobUserTimeLimit</b> as an enforceable limit and terminate processes in jobs that exceed the limit, see the <a href="/windows/desktop/api/winnt/ns-winnt-jobobject_basic_limit_information">JOBOBJECT_BASIC_LIMIT_INFORMATION</a> structure.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.JobHighMemoryLimit

If the <i>LimitFlags</i> parameter specifies <b>JOB_OBJECT_LIMIT_JOB_MEMORY_HIGH</b>, this member is the notification maximum limit for total virtual memory that can be committed by all processes in the job, in bytes. Otherwise, this member is ignored.

### -field DUMMYUNIONNAME.JobMemoryLimit

If the <i>LimitFlags</i> parameter specifies <b>JOB_OBJECT_LIMIT_JOB_MEMORY</b>, this member is the notification maximum limit for total virtual memory that can be committed by all processes in the job, in bytes. Otherwise, this member is ignored.

### -field DUMMYUNIONNAME2

### -field DUMMYUNIONNAME2.RateControlTolerance

If the <i>LimitFlags</i> parameter specifies <b>JOB_OBJECT_LIMIT_RATE_CONTROL</b>, this member specifies the extent to which a job can exceed its CPU rate control limits during the interval specified by the <b>RateControlToleranceInterval</b> member.  Otherwise, this member is ignored. 

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

### -field DUMMYUNIONNAME2.CpuRateControlTolerance

If the <i>LimitFlags</i> parameter specifies <b>JOB_OBJECT_LIMIT_CPU_RATE_CONTROL</b>, this member specifies the extent to which a job can exceed its CPU rate control limits during the interval specified by the <b>CpuRateControlToleranceInterval</b> member.  Otherwise, this member is ignored.

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

### -field DUMMYUNIONNAME3

### -field DUMMYUNIONNAME3.RateControlToleranceInterval

If the <i>LimitFlags</i> parameter specifies <b>JOB_OBJECT_LIMIT_RATE_CONTROL</b>, this member specifies the interval during which a job's CPU usage is monitored to determine whether the job has exceeded its CPU rate control limits. Otherwise, this member is ignored. 

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

### -field DUMMYUNIONNAME3.CpuRateControlToleranceInterval

If the <i>LimitFlags</i> parameter specifies <b>JOB_OBJECT_CPU_LIMIT_RATE_CONTROL</b>, this member specifies the interval during which a job's CPU usage is monitored to determine whether the job has exceeded its CPU rate control limits. Otherwise, this member is ignored. 

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
<td width="40%"><a id="JOB_OBJECT_LIMIT_JOB_MEMORY_HIGH"></a><a id="job_object_limit_job_memory_high"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_JOB_MEMORY_HIGH</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
Establishes the notification threshold for the job-wide sum of private committed memory for all processes associated with the job. The <b>JobHighMemoryLimit</b> member contains additional information.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMIT_JOB_MEMORY_LOW"></a><a id="job_object_limit_job_memory_low"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_JOB_MEMORY_LOW</b></dt>
<dt>0x00008000</dt>
</dl>
</td>
<td width="60%">
Establishes the notification minimum for the job-wide sum of private committed memory for all processes associated with the job. If this value is set, a notification is sent when the amount of private committed memory falls below this threshold. The <b>JobLowMemoryLimit</b> member contains additional information.

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
<td width="40%"><a id="JOB_OBJECT_LIMIT_CPU_RATE_CONTROL"></a><a id="job_object_limit_cpu_rate_control"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_CPU_RATE_CONTROL</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
Establishes the notification threshold for the CPU rate control limits established for the job. The <b>CpuRateControlTolerance</b> and <b>CpuRateControlToleranceInterval</b> members contain additional information.

CPU rate control limits are established by calling <a href="/windows/desktop/api/jobapi2/nf-jobapi2-setinformationjobobject">SetInformationJobObject</a> with the <b>JobObjectCpuRateInformationClass</b> information class. 

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
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMIT_IO_RATE_CONTROL"></a><a id="job_object_limit_io_rate_control"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_IO_RATE_CONTROL</b></dt>
<dt>0x00080000</dt>
</dl>
</td>
<td width="60%">
Establishes the notification threshold for the I/O rate control limits established for the job. The <b>IoRateControlTolerance</b> and <b>IoRateControlToleranceInterval</b> members contain additional information.

I/O rate control limits are established by calling <a href="/windows/desktop/api/jobapi2/nf-jobapi2-setioratecontrolinformationjobobject">SetIoRateControlInformationJobObject</a>. 

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMIT_NET_RATE_CONTROL"></a><a id="job_object_limit_net_rate_control"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_NET_RATE_CONTROL</b></dt>
<dt>0x00100000</dt>
</dl>
</td>
<td width="60%">
Establishes the notification threshold for the network rate control limits established for the job. The <b>NetRateControlTolerance</b> and <b>NetRateControlToleranceInterval</b> members contain additional information.

Network rate control limits are established by calling <a href="/windows/desktop/api/jobapi2/nf-jobapi2-setinformationjobobject">SetInformationJobObject</a> with the <b>JobObjectNetRateInformationClass</b> information class. 

</td>
</tr>
</table>

### -field IoRateControlTolerance

If the <i>LimitFlags</i> parameter specifies <b>JOB_OBJECT_LIMIT_IO_RATE_CONTROL</b>, this member specifies the extent to which a job can exceed its I/O rate control limits during the interval specified by the <b>IoRateControlToleranceInterval</b> member.  Otherwise, this member is ignored.

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
The job can exceed its I/O rate control limits for 20% of the tolerance interval.

</td>
</tr>
<tr>
<td width="40%"><a id="ToleranceMedium"></a><a id="tolerancemedium"></a><a id="TOLERANCEMEDIUM"></a><dl>
<dt><b>ToleranceMedium</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The job can exceed its I/O rate control limits for 40% of the tolerance interval.

</td>
</tr>
<tr>
<td width="40%"><a id="ToleranceHigh"></a><a id="tolerancehigh"></a><a id="TOLERANCEHIGH"></a><dl>
<dt><b>ToleranceHigh</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The job can exceed its I/O rate control limits for 60% of the tolerance interval.

</td>
</tr>
</table>

### -field JobLowMemoryLimit

If the <i>LimitFlags</i> parameter specifies <b>JOB_OBJECT_LIMIT_JOB_MEMORY_LOW</b>, this member is the notification limit minimum for the total virtual memory that can be committed by all processes in the job, in bytes. Otherwise, this member is ignored.

### -field IoRateControlToleranceInterval

If the <i>LimitFlags</i> parameter specifies <b>JOB_OBJECT_IO_LIMIT_RATE_CONTROL</b>, this member specifies the interval during which a job's I/O usage is monitored to determine whether the job has exceeded its I/O rate control limits. Otherwise, this member is ignored. 

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

### -field NetRateControlTolerance

If the <i>LimitFlags</i> parameter specifies <b>JOB_OBJECT_LIMIT_IO_RATE_CONTROL</b>, this member specifies the extent to which a job can exceed its network rate control limits during the interval specified by the <b>NetRateControlToleranceInterval</b> member.  Otherwise, this member is ignored.

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
The job can exceed its network rate control limits for 20% of the tolerance interval.

</td>
</tr>
<tr>
<td width="40%"><a id="ToleranceMedium"></a><a id="tolerancemedium"></a><a id="TOLERANCEMEDIUM"></a><dl>
<dt><b>ToleranceMedium</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The job can exceed its network rate control limits for 40% of the tolerance interval.

</td>
</tr>
<tr>
<td width="40%"><a id="ToleranceHigh"></a><a id="tolerancehigh"></a><a id="TOLERANCEHIGH"></a><dl>
<dt><b>ToleranceHigh</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The job can exceed its network rate control limits for 60% of the tolerance interval.

</td>
</tr>
</table>

### -field NetRateControlToleranceInterval

If the <i>LimitFlags</i> parameter specifies <b>JOB_OBJECT_NET_LIMIT_RATE_CONTROL</b>, this member specifies the interval during which a job's network usage is monitored to determine whether the job has exceeded its network rate control limits. Otherwise, this member is ignored. 

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

## -remarks

When a notification limit is exceeded, the system sends a <b>JOB_OBJECT_MSG_NOTIFICATION_LIMIT</b> message to the I/O completion port associated with the job. Processes in the job continue to run and can continue to allocate memory or transmit read or write bytes beyond the specified limits. 

When the application monitoring the I/O completion port receives a <b>JOB_OBJECT_MSG_NOTIFICATION_LIMIT</b> message, it must call <a href="/windows/desktop/api/jobapi2/nf-jobapi2-queryinformationjobobject">QueryInformationJobObject</a> with the <b>JobObjectLimitViolationInformation2</b> information class. Limit violation information is received in a <a href="/windows/desktop/api/winnt/ns-winnt-jobobject_limit_violation_information_2">JOBOBJECT_LIMIT_VIOLATION_INFORMATION_2</a> structure that contains information about all notification limits that were exceeded at the time of the query. The system will not send another <b>JOB_OBJECT_MSG_NOTIFICATION_LIMIT</b> message until after   <b>QueryInformationJobObject</b> is called.  

CPU rate control limits for a job are established in a <a href="/windows/desktop/api/winnt/ns-winnt-jobobject_cpu_rate_control_information">JOBOBJECT_CPU_RATE_CONTROL_INFORMATION</a> structure. The CPU rate control values in the <b>JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION_2</b> structure specify how much the job can exceed its established CPU rate control limits before notification is sent.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_cpu_rate_control_information">JOBOBJECT_CPU_RATE_CONTROL_INFORMATION</a>



<a href="/windows/desktop/api/jobapi2/ns-jobapi2-jobobject_io_rate_control_information">JOBOBJECT_IO_RATE_CONTROL_INFORMATION</a>



<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_limit_violation_information_2">JOBOBJECT_LIMIT_VIOLATION_INFORMATION_2</a>



<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_net_rate_control_information">JOBOBJECT_NET_RATE_CONTROL_INFORMATION</a>



<a href="/windows/desktop/api/jobapi2/nf-jobapi2-queryinformationjobobject">QueryInformationJobObject</a>



<a href="/windows/desktop/api/jobapi2/nf-jobapi2-setinformationjobobject">SetInformationJobObject</a>



<a href="/windows/desktop/api/jobapi2/nf-jobapi2-setioratecontrolinformationjobobject">SetIoRateControlInformationJobObject</a>