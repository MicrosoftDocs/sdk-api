---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _PRINT_OTHER_INFO structure


## -description


The
				<b>PRINT_OTHER_INFO</b> structure contains information about a print job. The 
<a href="https://msdn.microsoft.com/11367a72-c21d-4044-98cf-a7a30cc43a8b">NetAlertRaise</a> and 
<a href="https://msdn.microsoft.com/9762f0d6-0022-4e05-b2d8-6223d7bbb2c8">NetAlertRaiseEx</a> functions use the 
<b>PRINT_OTHER_INFO</b> structure to specify information when a job has finished printing, or when a printer needs intervention.


## -struct-fields




### -field alrtpr_jobid

Type: <b>DWORD</b>

The identification number of the print job.


### -field alrtpr_status

Type: <b>DWORD</b>

A bitmask describing the status of the print job. 




You can obtain the overall status of the job by checking PRJOB_QSTATUS (bits 0 and 1). 

Possible values for the print job status are listed in the <i>Lmalert.h</i> header file.


<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PRJOB_QS_QUEUED"></a><a id="prjob_qs_queued"></a><dl>
<dt><b>PRJOB_QS_QUEUED</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The print job is in the queue waiting to be scheduled.

</td>
</tr>
<tr>
<td width="40%"><a id="PRJOB_QS_PAUSED"></a><a id="prjob_qs_paused"></a><dl>
<dt><b>PRJOB_QS_PAUSED</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The print job is in the queue, but it has been paused. (When a job is paused, it cannot be scheduled.)

</td>
</tr>
<tr>
<td width="40%"><a id="PRJOB_QS_SPOOLING"></a><a id="prjob_qs_spooling"></a><dl>
<dt><b>PRJOB_QS_SPOOLING</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The print job is in the process of being spooled.

</td>
</tr>
<tr>
<td width="40%"><a id="PRJOB_QS_PRINTING"></a><a id="prjob_qs_printing"></a><dl>
<dt><b>PRJOB_QS_PRINTING</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The job is currently printing.

</td>
</tr>
</table>
 

If the print job is in the PRJOB_QS_PRINTING state, you can check bits 2 through 8 for the device's status (PRJOB_DEVSTATUS). Bit 15 is also meaningful.

Possible values for the device's status are listed in the <i>Lmalert.h</i> header file.


<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PRJOB_COMPLETE"></a><a id="prjob_complete"></a><dl>
<dt><b>PRJOB_COMPLETE</b></dt>
<dt>0x4</dt>
</dl>
</td>
<td width="60%">
The job has completed printing.

</td>
</tr>
<tr>
<td width="40%"><a id="PRJOB_INTERV"></a><a id="prjob_interv"></a><dl>
<dt><b>PRJOB_INTERV</b></dt>
<dt>0x8</dt>
</dl>
</td>
<td width="60%">
The destination printer requires an operator's intervention.

</td>
</tr>
<tr>
<td width="40%"><a id="PRJOB_ERROR"></a><a id="prjob_error"></a><dl>
<dt><b>PRJOB_ERROR</b></dt>
<dt>0x10</dt>
</dl>
</td>
<td width="60%">
There is an error at the destination printer.

</td>
</tr>
<tr>
<td width="40%"><a id="PRJOB_DESTOFFLINE"></a><a id="prjob_destoffline"></a><dl>
<dt><b>PRJOB_DESTOFFLINE</b></dt>
<dt>0x20</dt>
</dl>
</td>
<td width="60%">
The destination printer is offline.

</td>
</tr>
<tr>
<td width="40%"><a id="PRJOB_DESTPAUSED"></a><a id="prjob_destpaused"></a><dl>
<dt><b>PRJOB_DESTPAUSED</b></dt>
<dt>0x40</dt>
</dl>
</td>
<td width="60%">
The destination printer is paused.

</td>
</tr>
<tr>
<td width="40%"><a id="PRJOB_NOTIFY"></a><a id="prjob_notify"></a><dl>
<dt><b>PRJOB_NOTIFY</b></dt>
<dt>0x80</dt>
</dl>
</td>
<td width="60%">
A printing alert should be raised.

</td>
</tr>
<tr>
<td width="40%"><a id="PRJOB_DESTNOPAPER"></a><a id="prjob_destnopaper"></a><dl>
<dt><b>PRJOB_DESTNOPAPER</b></dt>
<dt>0x100</dt>
</dl>
</td>
<td width="60%">
The destination printer is out of paper.

</td>
</tr>
<tr>
<td width="40%"><a id="PRJOB_DELETED"></a><a id="prjob_deleted"></a><dl>
<dt><b>PRJOB_DELETED</b></dt>
<dt>0x8000</dt>
</dl>
</td>
<td width="60%">
The printing job is being deleted.

</td>
</tr>
</table>
 


### -field alrtpr_submitted

Type: <b>DWORD</b>

The time at which the print job was submitted. This value is stored as the number of seconds that have elapsed since 00:00:00, January 1, 1970, GMT.


### -field alrtpr_size

Type: <b>DWORD</b>

The size, in bytes, of the print job.


## -remarks



Additional variable-length data follows the 
<b>PRINT_OTHER_INFO</b> structure in the alert message buffer. The information is in the form of contiguous null-terminated character strings, as follows.


<table>
<tr>
<th>String</th>
<th>Meaning</th>
</tr>
<tr>
<td>computername</td>
<td>The computer that submitted the print job.</td>
</tr>
<tr>
<td>username</td>
<td>The user who submitted the print job.</td>
</tr>
<tr>
<td>queuename</td>
<td>The print queue to which the job was submitted.</td>
</tr>
<tr>
<td>destination</td>
<td>The printer destination (device) to which the print job was routed.</td>
</tr>
<tr>
<td>status</td>
<td>The status of the print job.</td>
</tr>
</table>
 



The calling application must allocate and free the memory for all structures and variable-length data in an alert message buffer.

See 
<a href="https://msdn.microsoft.com/9762f0d6-0022-4e05-b2d8-6223d7bbb2c8">NetAlertRaiseEx</a> for a code sample that demonstrates how to raise a print alert.




## -see-also




<a href="https://msdn.microsoft.com/43119dcf-7d04-4e3b-b1dc-20e814fbdc2f">ADMIN_OTHER_INFO</a>



<a href="https://msdn.microsoft.com/e131191b-7413-45ff-84cd-b3a873d33ca1">Alert Functions</a>



<a href="https://msdn.microsoft.com/832ebe88-e1c4-4ce3-8057-922419b577f7">ERRLOG_OTHER_INFO</a>



<a href="https://msdn.microsoft.com/11367a72-c21d-4044-98cf-a7a30cc43a8b">NetAlertRaise</a>



<a href="https://msdn.microsoft.com/9762f0d6-0022-4e05-b2d8-6223d7bbb2c8">NetAlertRaiseEx</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/daa4594f-e59e-4f05-8183-677bee4ea446">STD_ALERT</a>



<a href="https://msdn.microsoft.com/2f6bd906-fdab-410a-8856-4482e047371f">USER_OTHER_INFO</a>
 

 

