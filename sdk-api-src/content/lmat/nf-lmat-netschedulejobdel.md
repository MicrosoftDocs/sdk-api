---
UID: NF:lmat.NetScheduleJobDel
title: NetScheduleJobDel function
author: windows-sdk-content
description: The NetScheduleJobDel function deletes a range of jobs queued to run at a computer. This function requires that the schedule service be started at the computer to which the job deletion request is being sent.
old-location: netmgmt\netschedulejobdel.htm
old-project: netmgmt
ms.assetid: 5ae668ab-f51d-457e-a239-2ec16a0e5a55
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: NetScheduleJobDel, NetScheduleJobDel function [Network Management], _win32_netschedulejobdel, lmat/NetScheduleJobDel, netmgmt.netschedulejobdel
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
 - NetScheduleJobDel
product: Windows
targetos: Windows
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
req.product: GDI+ 1.1
---

# NetScheduleJobDel function


## -description


<p class="CCE_Message">[<b>NetScheduleJobDel</b> is no longer available for use as of Windows 8. Instead, use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e"> Task Scheduler 2.0 Interfaces</a>.

]

The
				<b>NetScheduleJobDel</b> function deletes a range of jobs queued to run at a computer. This function requires that the schedule service be started at the computer to which the job deletion request is being sent. 


## -parameters




### -param OPTIONAL

TBD


### -param MinJobId [in]

The minimum job identifier. Jobs with a job identifier smaller than <i>MinJobId</i> will not be deleted.


### -param MaxJobId [in]

The  maximum job identifier. Jobs with a job identifier larger than <i>MaxJobId</i> will not be deleted.


#### - Servername [in, optional]

A pointer to a constant string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used. 





## -returns



If the function succeeds, the return value is NERR_Success.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



Normally only members of the local Administrators group on the computer where the schedule job is being deleted can successfully execute this function. If the server name passed in the string pointed to by the <i>Servername</i> parameter is a remote server, then only members of the local Administrators group on the  server can successfully execute this function. 

If the following registry value has the least significant bit set (for example, 0x00000001), then users belonging to the Server Operators group can also successfully execute this function.


<b>HKLM\System\CurrentControlSet\Control\Lsa\SubmitControl</b>

Call the 
<a href="https://msdn.microsoft.com/e3384414-6a15-4979-bed4-6f94f046474a">NetScheduleJobEnum</a> function to retrieve the job identifier for one or more scheduled jobs.

The 
<b>NetScheduleJobDel</b> function deletes all jobs whose job identifiers are in the range <i>MinJobId</i> through <i>MaxJobId</i>.

To delete all scheduled jobs at the server, you can call 
<b>NetScheduleJobDel</b> specifying <i>MinJobId</i> equal to 0 and <i>MaxJobId</i> equal to – 1. To delete one job, specify the job's identifier for both the <i>MinJobId</i> parameter and the <i>MaxJobId</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/813d13ba-abe1-4b14-88c7-87ba88a42a3b">NetScheduleJobAdd</a>



<a href="https://msdn.microsoft.com/e3384414-6a15-4979-bed4-6f94f046474a">NetScheduleJobEnum</a>



<a href="https://msdn.microsoft.com/44589715-edab-4737-9e49-6f491fd44c28">NetScheduleJobGetInfo</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>



<a href="https://msdn.microsoft.com/1ddc9b95-fdbc-4e39-9b55-2a5bc570b95d">Schedule
		  Functions</a>
 

 

