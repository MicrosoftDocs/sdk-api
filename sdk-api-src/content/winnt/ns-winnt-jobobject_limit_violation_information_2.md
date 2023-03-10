---
UID: NS:winnt.JOBOBJECT_LIMIT_VIOLATION_INFORMATION_2
title: JOBOBJECT_LIMIT_VIOLATION_INFORMATION_2 (winnt.h)
description: Contains extended information about resource notification limits that have been exceeded for a job object. This structure is used with the QueryInformationJobObject function with the JobObjectLimitViolationInformation2 information class.
helpviewer_keywords: ["JOBOBJECT_LIMIT_VIOLATION_INFORMATION_2","JOBOBJECT_LIMIT_VIOLATION_INFORMATION_2 structure","JOB_OBJECT_LIMIT_CPU_RATE_CONTROL","JOB_OBJECT_LIMIT_IO_RATE_CONTROL","JOB_OBJECT_LIMIT_JOB_MEMORY_HIGH","JOB_OBJECT_LIMIT_JOB_MEMORY_LOW","JOB_OBJECT_LIMIT_JOB_READ_BYTES","JOB_OBJECT_LIMIT_JOB_TIME","JOB_OBJECT_LIMIT_JOB_WRITE_BYTES","JOB_OBJECT_LIMIT_NET_RATE_CONTROL","JOB_OBJECT_LIMIT_RATE_CONTROL","JOB_OBJECT_LIMIT_JOB_READ_BYTES","JOB_OBJECT_LIMIT_JOB_WRITE_BYTES","ToleranceHigh","ToleranceLow","ToleranceMedium","base.jobobject_limit_violation_information_2","winnt/JOBOBJECT_LIMIT_VIOLATION_INFORMATION_2"]
old-location: base\jobobject_limit_violation_information_2.htm
tech.root: backup
ms.assetid: B474F74E-B64B-4681-A235-C2DE317BFE0E
ms.date: 12/05/2018
ms.keywords: JOBOBJECT_LIMIT_VIOLATION_INFORMATION_2, JOBOBJECT_LIMIT_VIOLATION_INFORMATION_2 structure, JOB_OBJECT_LIMIT_CPU_RATE_CONTROL, JOB_OBJECT_LIMIT_IO_RATE_CONTROL, JOB_OBJECT_LIMIT_JOB_MEMORY_HIGH, JOB_OBJECT_LIMIT_JOB_MEMORY_LOW, JOB_OBJECT_LIMIT_JOB_READ_BYTES, JOB_OBJECT_LIMIT_JOB_TIME, JOB_OBJECT_LIMIT_JOB_WRITE_BYTES, JOB_OBJECT_LIMIT_NET_RATE_CONTROL, JOB_OBJECT_LIMIT_RATE_CONTROL, JOB_OBJECT_LIMIT_JOB_READ_BYTES, JOB_OBJECT_LIMIT_JOB_WRITE_BYTES, ToleranceHigh, ToleranceLow, ToleranceMedium, base.jobobject_limit_violation_information_2, winnt/JOBOBJECT_LIMIT_VIOLATION_INFORMATION_2
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
req.typenames: JOBOBJECT_LIMIT_VIOLATION_INFORMATION_2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - JOBOBJECT_LIMIT_VIOLATION_INFORMATION_2
 - winnt/JOBOBJECT_LIMIT_VIOLATION_INFORMATION_2
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
 - JOBOBJECT_LIMIT_VIOLATION_INFORMATION_2
---

# JOBOBJECT_LIMIT_VIOLATION_INFORMATION_2 structure


## -description

Contains extended information about resource notification limits that have been exceeded for a job object. This structure is used with the <a href="/windows/desktop/api/jobapi2/nf-jobapi2-queryinformationjobobject">QueryInformationJobObject</a> function with the <b>JobObjectLimitViolationInformation2</b> information class.

## -struct-fields

### -field LimitFlags

Flags that identify the notification limits in effect for the job. This member is a bitfield that determines whether other structure members are used. This member can be any combination of the following values.

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
The job has a committed memory notification limit. The <b>JobHighMemoryLimit</b> member contains more information.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMIT_JOB_MEMORY_LOW"></a><a id="job_object_limit_job_memory_low"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_JOB_MEMORY_LOW</b></dt>
<dt>0x00008000</dt>
</dl>
</td>
<td width="60%">
The job has a committed minimum memory notification limit. The <b>JobLowMemoryLimit</b> member contains more information.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMIT_JOB_READ_BYTES"></a><a id="job_object_limit_job_read_bytes"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_JOB_READ_BYTES</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
The job has an I/O read bytes notification limit. The <b>IoReadBytesLimit</b> member contains more information.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMIT_JOB_WRITE_BYTES"></a><a id="job_object_limit_job_write_bytes"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_JOB_WRITE_BYTES</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
The job has an I/O write bytes notification limit. The <b>IoWriteBytesLimit</b> member contains more information.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMIT_JOB_TIME"></a><a id="job_object_limit_job_time"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_JOB_TIME</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The job has a user-mode execution time notification limit. The <b>PerJobUserTimeLimit</b> member contains more information.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMIT_RATE_CONTROL"></a><a id="job_object_limit_rate_control"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_RATE_CONTROL</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
The job has notification limit for the extent to which a job can exceed its CPU rate control limit. The <b>RateControlToleranceLimit</b> member contains more information. 

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMIT_CPU_RATE_CONTROL"></a><a id="job_object_limit_cpu_rate_control"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_CPU_RATE_CONTROL</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
The job has notification limit for the extent to which a job can exceed its CPU rate control limit. The <b>CpuRateControlToleranceLimit</b> member contains more information. 

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMIT_IO_RATE_CONTROL"></a><a id="job_object_limit_io_rate_control"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_IO_RATE_CONTROL</b></dt>
<dt>0x00080000</dt>
</dl>
</td>
<td width="60%">
The job has notification limit for the extent to which a job can exceed its I/O rate control limit. The <b>IoRateControlToleranceLimit</b> member contains more information. 

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMIT_NET_RATE_CONTROL"></a><a id="job_object_limit_net_rate_control"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_NET_RATE_CONTROL</b></dt>
<dt>0x00100000</dt>
</dl>
</td>
<td width="60%">
The job has notification limit for the extent to which a job can exceed its network rate control limit. The <b>NetRateControlToleranceLimit</b> member contains more information. 

</td>
</tr>
</table>

### -field ViolationLimitFlags

Flags that identify the notification limits that have been exceeded. This member is a bitfield that determines whether other structure members are used. This member can be any combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMIT_JOB_READ_BYTES"></a><a id="job_object_limit_job_read_bytes"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_JOB_READ_BYTES</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
The job's I/O read bytes notification limit has been exceeded. The <b>IoReadBytes</b> member contains more information.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMI_JOB_WRITE_BYTES"></a><a id="job_object_limit_job_write_bytes"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_JOB_WRITE_BYTES</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
The job's I/O write bytes notification limit has been exceeded. The <b>IoWriteBytes</b> member contains more information.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMIT_JOB_TIME"></a><a id="job_object_limit_job_time"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_JOB_TIME</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The job's user-mode execution time notification limit has been exceeded. The <b>PerJobUserTime</b> member contains more information.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMIT_JOB_MEMORY_HIGH"></a><a id="job_object_limit_job_memory_high"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_JOB_MEMORY_HIGH</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
The job's committed maximum memory notification limit has been exceeded. The <b>JobMemory</b> member contains more information.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMIT_JOB_MEMORY_LOW"></a><a id="job_object_limit_job_memory_low"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_JOB_MEMORY_LOW</b></dt>
<dt>0x00008000</dt>
</dl>
</td>
<td width="60%">
The job's committed memory has fallen below its minimum notification limit. The <b>JobMemory</b> member contains more information.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMIT_RATE_CONTROL"></a><a id="job_object_limit_rate_control"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_RATE_CONTROL</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
The job's CPU rate control limit has been exceeded. The <b>RateControlTolerance</b> member contains more information. 

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMIT_CPU_RATE_CONTROL"></a><a id="job_object_limit_cpu_rate_control"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_CPU_RATE_CONTROL</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
The job's CPU rate control limit has been exceeded. The <b>CpuRateControlTolerance</b> member contains more information. 

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMIT_IO_RATE_CONTROL"></a><a id="job_object_limit_io_rate_control"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_IO_RATE_CONTROL</b></dt>
<dt>0x00080000</dt>
</dl>
</td>
<td width="60%">
The job's I/O rate control limit has been exceeded. The <b>IoRateControlTolerance</b> member contains more information. 

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMIT_NET_RATE_CONTROL"></a><a id="job_object_limit_net_rate_control"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_NET_RATE_CONTROL</b></dt>
<dt>0x00100000</dt>
</dl>
</td>
<td width="60%">
The job's network rate control limit has been exceeded. The <b>NetworkRateControlTolerance</b> member contains more information. 

</td>
</tr>
</table>

### -field IoReadBytes

If the <b>ViolationLimitFlags</b> member specifies <b>JOB_OBJECT_LIMIT_JOB_READ_BYTES</b>, this member contains the total I/O read bytes for all processes in the job at the time the notification was sent.

### -field IoReadBytesLimit

If the <b>LimitFlags</b> member specifies <b>JOB_OBJECT_LIMIT_JOB_READ_BYTES</b>, this member contains the I/O read bytes notification limit in effect for the job.

### -field IoWriteBytes

If the <b>ViolationLimitFlags</b> member specifies <b>JOB_OBJECT_LIMIT_JOB_WRITE_BYTES</b>, this member contains the total I/O write bytes for all processes in the job at the time the notification was sent.

### -field IoWriteBytesLimit

If the <b>LimitFlags</b> member specifies <b>JOB_OBJECT_LIMIT_JOB_WRITE_BYTES</b>, this member contains the I/O write bytes notification limit in effect for the job.

### -field PerJobUserTime

If the <b>ViolationLimitFlags</b> member specifies <b>JOB_OBJECT_LIMIT_JOB_TIME</b>, this member contains the total user-mode execution time for all processes in the job at the time the notification was sent.

### -field PerJobUserTimeLimit

If the <b>LimitFlags</b> member specifies <b>JOB_OBJECT_LIMIT_JOB_TIME</b>, this member contains the user-mode execution notification limit in effect for the job.

### -field JobMemory

If the <b>ViolationLimitFlags</b> member specifies <b>JOB_OBJECT_LIMIT_JOB_MEMORY_HIGH</b> or <b>JOB_OBJECT_LIMIT_JOB_MEMORY_LOW</b>, this member contains the committed memory for all processes in the job at the time the notification was sent.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.JobHighMemoryLimit

If the <b>LimitFlags</b> member specifies <b>JOB_OBJECT_LIMIT_JOB_MEMORY_HIGH</b>, this member contains the committed maximum memory limit in effect for the job.

### -field DUMMYUNIONNAME.JobMemoryLimit

If the <b>LimitFlags</b> member specifies <b>JOB_OBJECT_LIMIT_JOB_MEMORY</b>, this member contains the committed maximum memory limit in effect for the job.

### -field DUMMYUNIONNAME2

### -field DUMMYUNIONNAME2.RateControlTolerance

If the <b>LimitFlags</b> member specifies <b>JOB_OBJECT_LIMIT_RATE_CONTROL</b>, this member specifies the extent to which the job exceeded its CPU rate control limits at the time the notification was sent.  This member can be one of the following values. 

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
The job exceeded its CPU rate control limits for 20% of the tolerance interval.

</td>
</tr>
<tr>
<td width="40%"><a id="ToleranceMedium"></a><a id="tolerancemedium"></a><a id="TOLERANCEMEDIUM"></a><dl>
<dt><b>ToleranceMedium</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The job exceeded its CPU rate control limits for 40% of the tolerance interval.

</td>
</tr>
<tr>
<td width="40%"><a id="ToleranceHigh"></a><a id="tolerancehigh"></a><a id="TOLERANCEHIGH"></a><dl>
<dt><b>ToleranceHigh</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The job exceeded its CPU rate control limits for 60% of the tolerance interval.

</td>
</tr>
</table>

### -field DUMMYUNIONNAME2.CpuRateControlTolerance

If the <b>LimitFlags</b> member specifies <b>JOB_OBJECT_LIMIT_CPU_RATE_CONTROL</b>, this member specifies the extent to which the job exceeded its CPU rate control limits at the time the notification was sent.  This member can be one of the following values. 

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
The job exceeded its CPU rate control limits for 20% of the tolerance interval.

</td>
</tr>
<tr>
<td width="40%"><a id="ToleranceMedium"></a><a id="tolerancemedium"></a><a id="TOLERANCEMEDIUM"></a><dl>
<dt><b>ToleranceMedium</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The job exceeded its CPU rate control limits for 40% of the tolerance interval.

</td>
</tr>
<tr>
<td width="40%"><a id="ToleranceHigh"></a><a id="tolerancehigh"></a><a id="TOLERANCEHIGH"></a><dl>
<dt><b>ToleranceHigh</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The job exceeded its CPU rate control limits for 60% of the tolerance interval.

</td>
</tr>
</table>

### -field DUMMYUNIONNAME3

### -field DUMMYUNIONNAME3.RateControlToleranceLimit

If the <b>LimitFlags</b> member specifies <b>JOB_OBJECT_LIMIT_RATE_CONTROL</b>, this member contains the CPU rate control notification limits specified for the job.  

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

### -field DUMMYUNIONNAME3.CpuRateControlToleranceLimit

If the <i>LimitFlags</i> parameter specifies <b>JOB_OBJECT_LIMIT_CPU_RATE_CONTROL</b>, this member contains the CPU rate control notification limits specified for the job.  

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

### -field JobLowMemoryLimit

If the <b>LimitFlags</b> member specifies <b>JOB_OBJECT_LIMIT_JOB_MEMORY_LOW</b>, this member contains the committed minimum memory limit in effect for the job.

### -field IoRateControlTolerance

If the <b>LimitFlags</b> member specifies <b>JOB_OBJECT_LIMIT_IO_RATE_CONTROL</b>, this member specifies the extent to which the job exceeded its I/O rate control limits at the time the notification was sent.  This member can be one of the following values. 

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
The job exceeded its I/O rate control limits for 20% of the tolerance interval.

</td>
</tr>
<tr>
<td width="40%"><a id="ToleranceMedium"></a><a id="tolerancemedium"></a><a id="TOLERANCEMEDIUM"></a><dl>
<dt><b>ToleranceMedium</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The job exceeded its I/O rate control limits for 40% of the tolerance interval.

</td>
</tr>
<tr>
<td width="40%"><a id="ToleranceHigh"></a><a id="tolerancehigh"></a><a id="TOLERANCEHIGH"></a><dl>
<dt><b>ToleranceHigh</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The job exceeded its I/O rate control limits for 60% of the tolerance interval.

</td>
</tr>
</table>

### -field IoRateControlToleranceLimit

If the <i>LimitFlags</i> parameter specifies <b>JOB_OBJECT_LIMIT_IO_RATE_CONTROL</b>, this member contains the I/O rate control notification limits specified for the job.  

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

### -field NetRateControlTolerance

If the <b>LimitFlags</b> member specifies <b>JOB_OBJECT_LIMIT_NET_RATE_CONTROL</b>, this member specifies the extent to which the job exceeded its network rate control limits at the time the notification was sent.  This member can be one of the following values. 

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
The job exceeded its network rate control limits for 20% of the tolerance interval.

</td>
</tr>
<tr>
<td width="40%"><a id="ToleranceMedium"></a><a id="tolerancemedium"></a><a id="TOLERANCEMEDIUM"></a><dl>
<dt><b>ToleranceMedium</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The job exceeded its network rate control limits for 40% of the tolerance interval.

</td>
</tr>
<tr>
<td width="40%"><a id="ToleranceHigh"></a><a id="tolerancehigh"></a><a id="TOLERANCEHIGH"></a><dl>
<dt><b>ToleranceHigh</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The job exceeded its network rate control limits for 60% of the tolerance interval.

</td>
</tr>
</table>

### -field NetRateControlToleranceLimit

If the <i>LimitFlags</i> parameter specifies <b>JOB_OBJECT_LIMIT_NETWORK_RATE_CONTROL</b>, this member contains the network rate control notification limits specified for the job.  

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

## -remarks

When any notification limit specified in a <a href="/windows/desktop/api/winnt/ns-winnt-jobobject_notification_limit_information_2">JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION_2</a> structure is exceeded, the system sends a <b>JOB_OBJECT_MSG_NOTIFICATION_LIMIT</b> message to the I/O completion port associated with the job. 

To retrieve information about the limits that were exceeded, the application monitoring the I/O completion port must call the <a href="/windows/desktop/api/jobapi2/nf-jobapi2-queryinformationjobobject">QueryInformationJobObject</a> function with the <b>JobObjectLimitViolationInformation2</b> information class and a pointer to a <b>JOBOBJECT_LIMIT_VIOLATION_INFORMATION_2</b> structure.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_notification_limit_information_2">JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION_2</a>



<a href="/windows/desktop/api/jobapi2/nf-jobapi2-queryinformationjobobject">QueryInformationJobObject</a>



<a href="/windows/desktop/api/jobapi2/nf-jobapi2-setinformationjobobject">SetInformationJobObject</a>
