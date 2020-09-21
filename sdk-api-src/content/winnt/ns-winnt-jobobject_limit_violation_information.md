---
UID: NS:winnt._JOBOBJECT_LIMIT_VIOLATION_INFORMATION
title: JOBOBJECT_LIMIT_VIOLATION_INFORMATION (winnt.h)
description: Contains information about resource notification limits that have been exceeded for a job object. This structure is used with the QueryInformationJobObject function with the JobObjectLimitViolationInformation information class.
helpviewer_keywords: ["*PJOBOBJECT_LIMIT_VIOLATION_INFORMATION","JOBOBJECT_LIMIT_VIOLATION_INFORMATION","JOBOBJECT_LIMIT_VIOLATION_INFORMATION structure","JOB_OBJECT_LIMIT_JOB_MEMORY","JOB_OBJECT_LIMIT_JOB_READ_BYTES","JOB_OBJECT_LIMIT_JOB_TIME","JOB_OBJECT_LIMIT_JOB_WRITE_BYTES","JOB_OBJECT_LIMIT_RATE_CONTROL","JOB_OBJECT_LIMIT_READ_BYTES","JOB_OBJECT_LIMIT_WRITE_BYTES","PJOBOBJECT_LIMIT_VIOLATION_INFORMATION","PJOBOBJECT_LIMIT_VIOLATION_INFORMATION structure pointer","ToleranceHigh","ToleranceIntervalLong","ToleranceIntervalMedium","ToleranceIntervalShort","ToleranceLow","ToleranceMedium","_JOBOBJECT_LIMIT_VIOLATION_INFORMATION","base.jobobject_limit_violation_information","winnt/JOBOBJECT_LIMIT_VIOLATION_INFORMATION","winnt/PJOBOBJECT_LIMIT_VIOLATION_INFORMATION"]
old-location: base\jobobject_limit_violation_information.htm
tech.root: backup
ms.assetid: 445f21aa-ba42-4ad6-8d28-f7811a5d8a8c
ms.date: 12/05/2018
ms.keywords: '*PJOBOBJECT_LIMIT_VIOLATION_INFORMATION, JOBOBJECT_LIMIT_VIOLATION_INFORMATION, JOBOBJECT_LIMIT_VIOLATION_INFORMATION structure, JOB_OBJECT_LIMIT_JOB_MEMORY, JOB_OBJECT_LIMIT_JOB_READ_BYTES, JOB_OBJECT_LIMIT_JOB_TIME, JOB_OBJECT_LIMIT_JOB_WRITE_BYTES, JOB_OBJECT_LIMIT_RATE_CONTROL, JOB_OBJECT_LIMIT_READ_BYTES, JOB_OBJECT_LIMIT_WRITE_BYTES, PJOBOBJECT_LIMIT_VIOLATION_INFORMATION, PJOBOBJECT_LIMIT_VIOLATION_INFORMATION structure pointer, ToleranceHigh, ToleranceIntervalLong, ToleranceIntervalMedium, ToleranceIntervalShort, ToleranceLow, ToleranceMedium, _JOBOBJECT_LIMIT_VIOLATION_INFORMATION, base.jobobject_limit_violation_information, winnt/JOBOBJECT_LIMIT_VIOLATION_INFORMATION, winnt/PJOBOBJECT_LIMIT_VIOLATION_INFORMATION'
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
req.typenames: JOBOBJECT_LIMIT_VIOLATION_INFORMATION, *PJOBOBJECT_LIMIT_VIOLATION_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _JOBOBJECT_LIMIT_VIOLATION_INFORMATION
 - winnt/_JOBOBJECT_LIMIT_VIOLATION_INFORMATION
 - PJOBOBJECT_LIMIT_VIOLATION_INFORMATION
 - winnt/PJOBOBJECT_LIMIT_VIOLATION_INFORMATION
 - JOBOBJECT_LIMIT_VIOLATION_INFORMATION
 - winnt/JOBOBJECT_LIMIT_VIOLATION_INFORMATION
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
 - JOBOBJECT_LIMIT_VIOLATION_INFORMATION
---

# JOBOBJECT_LIMIT_VIOLATION_INFORMATION structure


## -description

Contains information about resource notification limits that have been exceeded for a job object. This structure is used with the <a href="/windows/desktop/api/jobapi2/nf-jobapi2-queryinformationjobobject">QueryInformationJobObject</a> function with the <b>JobObjectLimitViolationInformation</b> information class.

## -struct-fields

### -field LimitFlags

Flags that identify the notification limits in effect for the job. This member is a bitfield that determines whether other structure members are used. This member can be any combination of the following values.

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
The job has a committed memory notification limit. The <b>JobMemoryLimit</b> member contains more information.

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
<td width="40%"><a id="JOB_OBJECT_LIMIT_RATE_CONTROL"></a><a id="job_object_limit_rate_control"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_RATE_CONTROL</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
The extent to which a job can exceed its CPU rate control limit. The <b>RateControlToleranceLimit</b> member contains more information. 

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
<td width="40%"><a id="JOB_OBJECT_LIMIT_READ_BYTES"></a><a id="job_object_limit_read_bytes"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_READ_BYTES</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
The job's I/O read bytes notification limit has been exceeded. The <b>IoReadBytes</b> member contains more information.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_LIMIT_WRITE_BYTES"></a><a id="job_object_limit_write_bytes"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_WRITE_BYTES</b></dt>
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
<td width="40%"><a id="JOB_OBJECT_LIMIT_JOB_MEMORY"></a><a id="job_object_limit_job_memory"></a><dl>
<dt><b>JOB_OBJECT_LIMIT_JOB_MEMORY</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
The job's committed memory notification limit has been exceeded. The <b>JobMemory</b> member contains more information.

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
</table>

### -field IoReadBytes

If the ViolationLimitFlags member specifies JOB_OBJECT_LIMIT_READ_BYTES, this member contains the total I/O read bytes for all processes in the job at the time the notification was sent.

### -field IoReadBytesLimit

If the LimitFlags member specifies JOB_OBJECT_LIMIT_READ_BYTES, this member contains the I/O read bytes notification limit in effect for the job.

### -field IoWriteBytes

If the ViolationLimitFlags member specifies JOB_OBJECT_LIMIT_WRITE_BYTES, this member contains the total I/O write bytes for all processes in the job at the time the notification was sent.

### -field IoWriteBytesLimit

If the LimitFlags member specifies JOB_OBJECT_LIMIT_WRITE_BYTES, this member contains the I/O write bytes notification limit in effect for the job.

### -field PerJobUserTime

If the ViolationLimitFlags member specifies JOB_OBJECT_LIMIT_JOB_TIME, this member contains the total user-mode execution time for all processes in the job at the time the notification was sent.

### -field PerJobUserTimeLimit

If the LimitFlags member specifies JOB_OBJECT_LIMIT_JOB_TIME, this member contains the user-mode execution notification limit in effect for the job.

### -field JobMemory

If the ViolationLimitFlags member specifies JOB_OBJECT_LIMIT_JOB_MEMORY, this member contains the committed memory for all processes in the job at the time the notification was sent.

### -field JobMemoryLimit

If the LimitFlags member specifies JOB_OBJECT_LIMIT_JOB_MEMORY, this member contains the committed memory limit in effect for the job.

### -field RateControlTolerance

If the <i>LimitFlags</i> parameter specifies JOB_OBJECT_LIMIT_RATE_CONTROL, this member specifies the extent to which the job exceeded its CPU rate control limits at the time the notification was sent.  This member can be one of the following values. 

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

### -field RateControlToleranceLimit

If the <i>LimitFlags</i> parameter specifies JOB_OBJECT_LIMIT_RATE_CONTROL, this member contains the CPU rate control notification limits specified for the job.  

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="_ToleranceIntervalShort"></a><a id="_toleranceintervalshort"></a><a id="_TOLERANCEINTERVALSHORT"></a><dl>
<dt><b> ToleranceIntervalShort</b></dt>
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

When any notification limit specified in a JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION structure is exceeded, the system sends a JOB_OBJECT_MSG_NOTIFICATION_LIMIT message to the I/O completion port associated with the job.

To retrieve information about the limits that were exceeded, the application monitoring the I/O completion port must call the <a href="/windows/desktop/api/jobapi2/nf-jobapi2-queryinformationjobobject">QueryInformationJobObject</a> function with the <b>JobObjectLimitViolationInformation</b> information class and a pointer to a <b>JOBOBJECT_LIMIT_VIOLATION_INFORMATION</b> structure.

## -see-also

<a href="/windows/desktop/api/jobapi2/nf-jobapi2-queryinformationjobobject">QueryInformationJobObject</a>



<a href="/windows/desktop/api/jobapi2/nf-jobapi2-setinformationjobobject">SetInformationJobObject</a>