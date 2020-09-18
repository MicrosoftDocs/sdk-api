---
UID: NS:winnt._JOBOBJECT_CPU_RATE_CONTROL_INFORMATION
title: JOBOBJECT_CPU_RATE_CONTROL_INFORMATION (winnt.h)
description: Contains CPU rate control information for a job object. This structure is used by the SetInformationJobObject and QueryInformationJobObject functions with the JobObjectCpuRateControlInformation information class.
helpviewer_keywords: ["*PJOBOBJECT_CPU_RATE_CONTROL_INFORMATION","JOBOBJECT_CPU_RATE_CONTROL_INFORMATION","JOBOBJECT_CPU_RATE_CONTROL_INFORMATION structure","JOB_OBJECT_ CPU_RATE_CONTROL_MIN_MAX_RATE","JOB_OBJECT_CPU_RATE_CONTROL_ENABLE","JOB_OBJECT_CPU_RATE_CONTROL_HARD_CAP","JOB_OBJECT_CPU_RATE_CONTROL_NOTIFY","JOB_OBJECT_CPU_RATE_CONTROL_WEIGHT_BASED","PJOBOBJECT_CPU_RATE_CONTROL_INFORMATION","PJOBOBJECT_CPU_RATE_CONTROL_INFORMATION structure pointer","_JOBOBJECT_CPU_RATE_CONTROL_INFORMATION","base.jobobject_cpu_rate_control_information","winnt/JOBOBJECT_CPU_RATE_CONTROL_INFORMATION","winnt/PJOBOBJECT_CPU_RATE_CONTROL_INFORMATION"]
old-location: base\jobobject_cpu_rate_control_information.htm
tech.root: backup
ms.assetid: eaa5bda2-a37e-441b-a0e4-e00dff6425b2
ms.date: 12/05/2018
ms.keywords: '*PJOBOBJECT_CPU_RATE_CONTROL_INFORMATION, JOBOBJECT_CPU_RATE_CONTROL_INFORMATION, JOBOBJECT_CPU_RATE_CONTROL_INFORMATION structure, JOB_OBJECT_ CPU_RATE_CONTROL_MIN_MAX_RATE, JOB_OBJECT_CPU_RATE_CONTROL_ENABLE, JOB_OBJECT_CPU_RATE_CONTROL_HARD_CAP, JOB_OBJECT_CPU_RATE_CONTROL_NOTIFY, JOB_OBJECT_CPU_RATE_CONTROL_WEIGHT_BASED, PJOBOBJECT_CPU_RATE_CONTROL_INFORMATION, PJOBOBJECT_CPU_RATE_CONTROL_INFORMATION structure pointer, _JOBOBJECT_CPU_RATE_CONTROL_INFORMATION, base.jobobject_cpu_rate_control_information, winnt/JOBOBJECT_CPU_RATE_CONTROL_INFORMATION, winnt/PJOBOBJECT_CPU_RATE_CONTROL_INFORMATION'
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
req.typenames: JOBOBJECT_CPU_RATE_CONTROL_INFORMATION, *PJOBOBJECT_CPU_RATE_CONTROL_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _JOBOBJECT_CPU_RATE_CONTROL_INFORMATION
 - winnt/_JOBOBJECT_CPU_RATE_CONTROL_INFORMATION
 - PJOBOBJECT_CPU_RATE_CONTROL_INFORMATION
 - winnt/PJOBOBJECT_CPU_RATE_CONTROL_INFORMATION
 - JOBOBJECT_CPU_RATE_CONTROL_INFORMATION
 - winnt/JOBOBJECT_CPU_RATE_CONTROL_INFORMATION
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
 - JOBOBJECT_CPU_RATE_CONTROL_INFORMATION
---

# JOBOBJECT_CPU_RATE_CONTROL_INFORMATION structure


## -description

Contains CPU rate control information for a job object. This structure is used by the <a href="/windows/desktop/api/jobapi2/nf-jobapi2-setinformationjobobject">SetInformationJobObject</a> and <a href="/windows/desktop/api/jobapi2/nf-jobapi2-queryinformationjobobject">QueryInformationJobObject</a> functions with the <b>JobObjectCpuRateControlInformation</b> information class.

## -struct-fields

### -field ControlFlags

The scheduling policy for CPU rate control. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_CPU_RATE_CONTROL_ENABLE"></a><a id="job_object_cpu_rate_control_enable"></a><dl>
<dt><b>JOB_OBJECT_CPU_RATE_CONTROL_ENABLE</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
This flag enables the job's CPU rate to be controlled based on weight or hard cap. You must set this value if you also set <b>JOB_OBJECT_CPU_RATE_CONTROL_WEIGHT_BASED</b>,   <b>JOB_OBJECT_CPU_RATE_CONTROL_HARD_CAP</b>, or <b>JOB_OBJECT_CPU_RATE_CONTROL_MIN_MAX_RATE</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_CPU_RATE_CONTROL_WEIGHT_BASED"></a><a id="job_object_cpu_rate_control_weight_based"></a><dl>
<dt><b>JOB_OBJECT_CPU_RATE_CONTROL_WEIGHT_BASED</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
The job's CPU rate is calculated based on its relative weight to the weight of other jobs. If this flag is set, the <b>Weight</b> member contains more information. If this flag is clear, the <b>CpuRate</b> member contains more information.

If you set <b>JOB_OBJECT_CPU_RATE_CONTROL_WEIGHT_BASED</b>, you cannot also set <b>JOB_OBJECT_CPU_RATE_CONTROL_MIN_MAX_RATE</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_CPU_RATE_CONTROL_HARD_CAP"></a><a id="job_object_cpu_rate_control_hard_cap"></a><dl>
<dt><b>JOB_OBJECT_CPU_RATE_CONTROL_HARD_CAP</b></dt>
<dt>0x4</dt>
</dl>
</td>
<td width="60%">
The job's CPU rate is a hard limit. After the job reaches its CPU cycle limit for the current scheduling interval, no threads associated with the job will run until the next interval. 

If you set <b>JOB_OBJECT_CPU_RATE_CONTROL_HARD_CAP</b>, you cannot also set <b>JOB_OBJECT_CPU_RATE_CONTROL_MIN_MAX_RATE</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_CPU_RATE_CONTROL_NOTIFY"></a><a id="job_object_cpu_rate_control_notify"></a><dl>
<dt><b>JOB_OBJECT_CPU_RATE_CONTROL_NOTIFY</b></dt>
<dt>0x8</dt>
</dl>
</td>
<td width="60%">
Sends messages when the CPU rate for the job exceeds the rate limits for the job during the tolerance interval.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT__CPU_RATE_CONTROL_MIN_MAX_RATE"></a><a id="job_object__cpu_rate_control_min_max_rate"></a><dl>
<dt><b>JOB_OBJECT_ CPU_RATE_CONTROL_MIN_MAX_RATE</b></dt>
<dt>0x10</dt>
</dl>
</td>
<td width="60%">
The CPU rate for the job is limited by minimum and maximum rates that you specify in the <b>MinRate</b> and <b>MaxRate</b> members.

If you set <b>JOB_OBJECT_CPU_RATE_CONTROL_MIN_MAX_RATE</b>, you can set neither  <b>JOB_OBJECT_CPU_RATE_CONTROL_WEIGHT_BASED</b> nor <b>JOB_OBJECT_CPU_RATE_CONTROL_HARD_CAP</b>.

</td>
</tr>
</table>

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.CpuRate

Specifies the portion of processor cycles that the threads in a job object can use during each scheduling interval, as the number of cycles per 10,000 cycles. If the <b>ControlFlags</b> member specifies <b>JOB_OBJECT_CPU_RATE_WEIGHT_BASED</b> or <b>JOB_OBJECT_CPU_RATE_CONTROL_MIN_MAX_RATE</b>, this member is not used.

Set <b>CpuRate</b> to a percentage times 100. For example, to let the job use 20% of the CPU, set <b>CpuRate</b> to 20 times 100, or 2,000.

Do not set <b>CpuRate</b> to 0. If <b>CpuRate</b> is 0,  <a href="/windows/desktop/api/jobapi2/nf-jobapi2-setinformationjobobject">SetInformationJobObject</a> returns <b>INVALID_ARGS</b>.

### -field DUMMYUNIONNAME.Weight

If the <b>ControlFlags</b> member specifies <b>JOB_OBJECT_CPU_RATE_WEIGHT_BASED</b>, this member specifies the scheduling weight of the job object, which determines the share of processor time given to the job relative to other workloads on the processor. 

This member can be a value from 1 through 9, where 1 is the smallest share and 9 is the largest share. The default is 5, which should be used for most workloads.  

If the <b>ControlFlags</b> member specifies <b>JOB_OBJECT_CPU_RATE_CONTROL_MIN_MAX_RATE</b>, this member is not used.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.MinRate

Specifies the minimum portion of the processor cycles that the threads in a job object can reserve during each scheduling interval. Specify this rate as a percentage times 100.  For example, to set a minimum rate of 50%, specify 50 times 100, or  5,000.

For the minimum rates to work correctly, the sum of the minimum rates for all of the job objects in the system cannot exceed 10,000, which is the equivalent of 100%.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.MaxRate

Specifies the maximum portion of processor cycles that the threads in a job object can use during each scheduling interval. Specify this rate as a percentage times 100.  For example, to set  a maximum rate of 50%, specify 50 times 100, or  5,000.

After the job reaches this limit for a scheduling interval, no threads associated with the job can run until the next scheduling interval.

## -remarks

You can set CPU rate control for multiple jobs in a  hierarchy of nested jobs. When you set CPU rate control for a job object, the settings apply to the job and its child jobs in the hierarchy. When you set CPU rate control for a job in a nested hierarchy, the system calculates the corresponding quotas with respect to the CPU rate control of the immediate parent job for the job. In other words, the rates set for the job represent its portion of the CPU rate that is allocated to its parent job.  If a job object does not have a parent with CPU rate control turned on in the chain of its parent jobs, the rate control for the job represents the portion of the CPU for the entire system.

CPU rate control cannot be used by job objects in applications running under <a href="/windows/desktop/TermServ/terminal-services-portal">Remote Desktop Services</a> (formerly Terminal Services)  if Dynamic Fair Share Scheduling (DFSS) is in effect.

## -see-also

<a href="/windows/win32/api/winnt/ns-winnt-jobobject_notification_limit_information">JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION</a>



<a href="/windows/desktop/api/jobapi2/nf-jobapi2-queryinformationjobobject">QueryInformationJobObject</a>



<a href="/windows/desktop/api/jobapi2/nf-jobapi2-setinformationjobobject">SetInformationJobObject</a>