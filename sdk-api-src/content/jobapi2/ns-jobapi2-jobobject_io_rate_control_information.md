---
UID: NS:jobapi2.JOBOBJECT_IO_RATE_CONTROL_INFORMATION
title: JOBOBJECT_IO_RATE_CONTROL_INFORMATION (jobapi2.h)
description: Contains information used to control the I/O rate for a job. This structure is used by the SetIoRateControlInformationJobObject and QueryIoRateControlInformationJobObject functions.
helpviewer_keywords: ["JOBOBJECT_IO_RATE_CONTROL_INFORMATION","JOBOBJECT_IO_RATE_CONTROL_INFORMATION structure","JOB_OBJECT_IO_RATE_CONTROL_ENABLE","base.jobobject_io_rate_control_information","jobapi2/JOBOBJECT_IO_RATE_CONTROL_INFORMATION"]
old-location: base\jobobject_io_rate_control_information.htm
tech.root: backup
ms.assetid: E4AA03B5-4D83-4826-B85D-FA4B412AFEBF
ms.date: 01/09/2025
ms.keywords: JOBOBJECT_IO_RATE_CONTROL_INFORMATION, JOBOBJECT_IO_RATE_CONTROL_INFORMATION structure, JOB_OBJECT_IO_RATE_CONTROL_ENABLE, base.jobobject_io_rate_control_information, jobapi2/JOBOBJECT_IO_RATE_CONTROL_INFORMATION
req.header: jobapi2.h
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
req.typenames: JOBOBJECT_IO_RATE_CONTROL_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - JOBOBJECT_IO_RATE_CONTROL_INFORMATION
 - jobapi2/JOBOBJECT_IO_RATE_CONTROL_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - jobapi2.h
api_name:
 - JOBOBJECT_IO_RATE_CONTROL_INFORMATION
---

## -description

**Windows 10, version 1607, and newer: This structure is not supported.**

Contains information used to control the I/O rate for a job. This structure is used by the <a href="/windows/desktop/api/jobapi2/nf-jobapi2-setioratecontrolinformationjobobject">SetIoRateControlInformationJobObject</a> and <a href="/windows/desktop/api/jobapi2/nf-jobapi2-queryioratecontrolinformationjobobject">QueryIoRateControlInformationJobObject</a> functions.

## -struct-fields

### -field MaxIops

The maximum limit for the I/O rate in I/O operations per second (IOPS). Set to 0 if to specify no limit.

When you set both <b>MaxIops</b> and <b>MaxBandwith</b>, the operating system enforces the first limit that the I/O rate reaches.

### -field MaxBandwidth

The maximum limit for the I/O rate in bytes per second. Set to 0 to specify no limit.

When you set both <b>MaxBandwith</b> and <b>MaxIops</b>, the operating system enforces the first limit that the I/O rate reaches.

### -field ReservationIops

Sets a minimum I/O rate which the operating system reserves for the job. To make no reservation for the job, set this value to 0.

The operating system allows the job to perform I/O operations at this rate, if possible. If the sum of the minimum rates for all jobs exceeds the capacity of the operating system, the rate at which the operating system allows each job to perform I/O operations is proportional to the reservation for the job.

### -field VolumeName

The NT device name for the volume to which you want to apply the policy for the I/O rate. For information about NT device names, see <a href="/windows-hardware/drivers/kernel/nt-device-names">NT Device Names</a>.

If this member is <b>NULL</b>, the policy for the I/O rate applies to all of the volumes for the operating system. For example, if this member is <b>NULL</b> and the <b>MaxIops</b> member is 100, the maximum limit for the I/O rate for each volume is set to 100 IOPS, instead of setting an aggregate limit for the I/O rate across all volumes of 100 IOPS.

### -field BaseIoSize

The base size of the normalized I/O unit, in bytes.  For example, if the <b>BaseIoSize</b> member is 8,000, every 8,000 bytes counts as one I/O unit. 4,000 bytes is also one I/O unit in this example, while 8,001 bytes is two I/O units.

You  can set the value of this base I/O size by using the <b>StorageBaseIOSize</b> value of the <b>HKEY_LOCAL_MACHINE</b>&#92;<b>SYSTEM</b>&#92;<b>CurrentControlSet</b>&#92;<b>Control</b>&#92;<b>QoS</b></p> registry key.

The value of the <b>BaseIoSize</b> member is subject to the following constraints:

<ul>
<li>The <a href="/windows/desktop/api/jobapi2/nf-jobapi2-setioratecontrolinformationjobobject">SetIoRateControlInformationJobObject</a> function requires that the <b>BaseIoSize</b> member of the <b>JOBOBJECT_IO_RATE_CONTROL_INFORMATION</b> structure that you pass to the function is  0.</li>
<li>The <a href="/windows/desktop/api/jobapi2/nf-jobapi2-queryioratecontrolinformationjobobject">QueryIoRateControlInformationJobObject</a> method sets the <b>BaseIoSize</b> member of this structure to 0 if the volume that the <b>VolumeName</b> member specifies does not support the control of the I/O rate.</li>
<li>The <a href="/windows/desktop/api/jobapi2/nf-jobapi2-queryioratecontrolinformationjobobject">QueryIoRateControlInformationJobObject</a> method sets the <b>BaseIoSize</b> member of this structure to the base size of the normalized I/O unit   if the volume that the <b>VolumeName</b> member specifies does support the control of the I/O rate.</li>
</ul>
To query for the base size of the normalized I/O unit without creating a job, call <a href="/windows/desktop/api/jobapi2/nf-jobapi2-queryioratecontrolinformationjobobject">QueryIoRateControlInformationJobObject</a> with the <i>hJob</i> parameter set to <b>NULL</b> from a process that is not associated with a job.

### -field ControlFlags

The policy for control of the I/O rate. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_IO_RATE_CONTROL_ENABLE"></a><a id="job_object_io_rate_control_enable"></a><dl>
<dt><b>JOB_OBJECT_IO_RATE_CONTROL_ENABLE</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
Turns on control of the I/O rate for the job when this structure is passed to the <a href="/windows/desktop/api/jobapi2/nf-jobapi2-setioratecontrolinformationjobobject">SetIoRateControlInformationJobObject</a> function. Indicates that control of the I/O rate for the job is turned on when this structure is used with the <a href="/windows/desktop/api/jobapi2/nf-jobapi2-queryioratecontrolinformationjobobject">QueryIoRateControlInformationJobObject</a> function.

</td>
</tr>
</table>

## -remarks

You can only set one I/O rate control for a job in a hierarchy of nested jobs. The settings that you specify apply to that job and the child jobs in the hierarchy for that job.  The settings do not apply to the chain of jobs from the parent job up to the top of the hierarchy. You still can change the settings for the original job in the hierarchy on which you set I/O rate control. However, attempts to set values for the control of the I/O rate for any other jobs in the hierarchy, including the parent jobs, fail.

## -see-also

<a href="/windows/desktop/api/jobapi2/nf-jobapi2-queryioratecontrolinformationjobobject">QueryIoRateControlInformationJobObject</a>



<a href="/windows/desktop/api/jobapi2/nf-jobapi2-setioratecontrolinformationjobobject">SetIoRateControlInformationJobObject</a>
