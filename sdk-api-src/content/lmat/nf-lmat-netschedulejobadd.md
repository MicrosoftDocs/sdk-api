---
UID: NF:lmat.NetScheduleJobAdd
title: NetScheduleJobAdd function
author: windows-sdk-content
description: The NetScheduleJobAdd function submits a job to run at a specified future time and date. This function requires that the schedule service be started on the computer to which the job is submitted.
old-location: netmgmt\netschedulejobadd.htm
old-project: netmgmt
ms.assetid: 813d13ba-abe1-4b14-88c7-87ba88a42a3b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: NetScheduleJobAdd, NetScheduleJobAdd function [Network Management], _win32_netschedulejobadd, lmat/NetScheduleJobAdd, netmgmt.netschedulejobadd
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: lmat.h
req.include-header: Lmat.h
req.redist: 
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
tech.root: 
req.typenames: USER_OTHER_INFO, *PUSER_OTHER_INFO, *LPUSER_OTHER_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetScheduleJobAdd
product: Windows
targetos: Windows
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
req.product: GDI+ 1.1
---

# NetScheduleJobAdd function


## -description


<p class="CCE_Message">[<b>NetScheduleJobAdd</b> is no longer available for use as of Windows 8. Instead, use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e"> Task Scheduler 2.0 Interfaces</a>.

]

The
				<b>NetScheduleJobAdd</b> function submits a job to run at a specified future time and date. This function requires that the schedule service be started on  the computer to which the job is submitted.
		


## -parameters




### -param OPTIONAL

TBD


### -param Buffer [in]

A pointer to an 
<a href="https://msdn.microsoft.com/eb0bf696-53ca-432a-b04c-5e0b6a61a0fd">AT_INFO</a> structure describing the job to submit. For more information about scheduling jobs using different job properties, see the following Remarks section and 
<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a>.


### -param JobId [out]

A pointer that receives a job identifier for the newly submitted job. This entry is valid only if the function returns successfully.


#### - Servername [in, optional]

A pointer to a constant string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.


## -returns



If the function succeeds, the return value is NERR_Success.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



Normally only members of the local Administrators group on the computer where the schedule job is being added can successfully execute this function. If the server name passed in the string pointed to by the <i>Servername</i> parameter is a remote server, then only members of the local Administrators group on the  remote server can successfully execute this function. 

If the following registry value has the least significant bit set (for example, 0x00000001), then users belonging to the Server Operators group can also successfully execute this function.


<b>HKLM\System\CurrentControlSet\Control\Lsa\SubmitControl</b>

The following are examples of how to schedule jobs using different properties supported by the 
<b>NetScheduleJobAdd</b> function.

To schedule a job that executes once:

<ul>
<li>Set the <b>DaysOfMonth</b> member of the 
<a href="https://msdn.microsoft.com/eb0bf696-53ca-432a-b04c-5e0b6a61a0fd">AT_INFO</a> structure to zero.</li>
<li>Set the <b>DaysOfWeek</b> member of the 
<a href="https://msdn.microsoft.com/eb0bf696-53ca-432a-b04c-5e0b6a61a0fd">AT_INFO</a> structure to zero.</li>
<li>Set the <b>JobTime</b> member of the 
<a href="https://msdn.microsoft.com/eb0bf696-53ca-432a-b04c-5e0b6a61a0fd">AT_INFO</a> structure to the time the job should execute.</li>
</ul>
The job executes at the time specified by the <b>JobTime</b> member of the 
<a href="https://msdn.microsoft.com/eb0bf696-53ca-432a-b04c-5e0b6a61a0fd">AT_INFO</a> structure pointed to by the <i>Buffer</i> parameter. After the job executes, it is deleted.

To schedule and delete a job that executes multiple times:

<ul>
<li>Set the appropriate bits in the  <b>DaysOfMonth</b> member of the 
<a href="https://msdn.microsoft.com/eb0bf696-53ca-432a-b04c-5e0b6a61a0fd">AT_INFO</a> structure or </li>
<li>Set the appropriate bits in the  <b>DaysOfWeek</b> member of the 
<a href="https://msdn.microsoft.com/eb0bf696-53ca-432a-b04c-5e0b6a61a0fd">AT_INFO</a> structure. </li>
<li>Set the <b>JobTime</b> member of the 
<a href="https://msdn.microsoft.com/eb0bf696-53ca-432a-b04c-5e0b6a61a0fd">AT_INFO</a> structure to the time the job should execute.</li>
</ul>
<div class="alert"><b>Note</b>  You do not need to set both the  <b>DaysOfMonth</b> and the  <b>DaysOfWeek</b> members of the 
<a href="https://msdn.microsoft.com/eb0bf696-53ca-432a-b04c-5e0b6a61a0fd">AT_INFO</a> structure.</div>
<div> </div>
The job executes at the time specified by the <b>JobTime</b> member of the 
<a href="https://msdn.microsoft.com/eb0bf696-53ca-432a-b04c-5e0b6a61a0fd">AT_INFO</a> structure pointed to by the <i>Buffer</i> parameter, once for each day set in the  <b>DaysOfMonth</b> or <b>DaysOfWeek</b> members of the 
<a href="https://msdn.microsoft.com/eb0bf696-53ca-432a-b04c-5e0b6a61a0fd">AT_INFO</a> structure. After each job executes, the corresponding bit is cleared. When the last bit is cleared, the job is deleted.

To schedule a job that executes periodically:

<ul>
<li>Set the appropriate bits in the <b>DaysOfMonth</b> member of the 
<a href="https://msdn.microsoft.com/eb0bf696-53ca-432a-b04c-5e0b6a61a0fd">AT_INFO</a> structure or</li>
<li>Set the appropriate bits in the <b>DaysOfWeek</b> member of the 
<a href="https://msdn.microsoft.com/eb0bf696-53ca-432a-b04c-5e0b6a61a0fd">AT_INFO</a> structure. </li>
<li>Set the <b>JobTime</b> member of the 
<a href="https://msdn.microsoft.com/eb0bf696-53ca-432a-b04c-5e0b6a61a0fd">AT_INFO</a> structure to the time the job should execute.</li>
<li>Set the job submission flag JOB_RUN_PERIODICALLY in the <b>Flags</b> member of the 
<a href="https://msdn.microsoft.com/eb0bf696-53ca-432a-b04c-5e0b6a61a0fd">AT_INFO</a> structure.</li>
</ul>
<div class="alert"><b>Note</b>  You do not need to set both the  <b>DaysOfMonth</b> and the  <b>DaysOfWeek</b> members of the 
<a href="https://msdn.microsoft.com/eb0bf696-53ca-432a-b04c-5e0b6a61a0fd">AT_INFO</a> structure.</div>
<div> </div>
The job will execute periodically, at the time specified by the <b>JobTime</b> member of the 
<a href="https://msdn.microsoft.com/eb0bf696-53ca-432a-b04c-5e0b6a61a0fd">AT_INFO</a> structure pointed to by the <i>Buffer</i> parameter, on each day set in the <b>DaysOfMonth</b> or <b>DaysOfWeek</b> member of the 
<a href="https://msdn.microsoft.com/eb0bf696-53ca-432a-b04c-5e0b6a61a0fd">AT_INFO</a> structure. The job will not be deleted as a result of the repeated executions. The only way to delete the job is by an explicit call to the 
<a href="https://msdn.microsoft.com/5ae668ab-f51d-457e-a239-2ec16a0e5a55">NetScheduleJobDel</a> function.

See 
the <a href="https://msdn.microsoft.com/eb0bf696-53ca-432a-b04c-5e0b6a61a0fd">AT_INFO</a> structure for a description of the <b>DaysOfWeek</b>, <b>DaysOfMonth</b>, and  job property bitmasks.

On Windows 2000, the earlier AT service and the Task Scheduler were combined. The Task Scheduler service was only accurate to the minute.  Therefore, the <b>NetScheduleJobAdd</b> function only uses hours and minutes specified in the <b>JobTime</b> member of the <a href="https://msdn.microsoft.com/eb0bf696-53ca-432a-b04c-5e0b6a61a0fd">AT_INFO</a> structure when a job is scheduled to run. 

Starting with   Windows Vista, the precision for the Task Scheduler was increased to the second. Therefore, the <b>NetScheduleJobAdd</b> function uses only the hours, minutes, and seconds specified in the <b>JobTime</b> member of the <a href="https://msdn.microsoft.com/eb0bf696-53ca-432a-b04c-5e0b6a61a0fd">AT_INFO</a> structure when a job is scheduled to run. 




## -see-also




<a href="https://msdn.microsoft.com/eb0bf696-53ca-432a-b04c-5e0b6a61a0fd">AT_INFO</a>



<a href="https://msdn.microsoft.com/5ae668ab-f51d-457e-a239-2ec16a0e5a55">NetScheduleJobDel</a>



<a href="https://msdn.microsoft.com/e3384414-6a15-4979-bed4-6f94f046474a">NetScheduleJobEnum</a>



<a href="https://msdn.microsoft.com/44589715-edab-4737-9e49-6f491fd44c28">NetScheduleJobGetInfo</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>



<a href="https://msdn.microsoft.com/1ddc9b95-fdbc-4e39-9b55-2a5bc570b95d">Schedule
		  Functions</a>
 

 

