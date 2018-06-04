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

# __MIDL_IBackgroundCopyJob_0002 enumeration


## -description


The 
<b>BG_JOB_STATE</b> enumeration defines constant values for the different states of a job.


## -enum-fields




### -field BG_JOB_STATE_QUEUED

Specifies that the job is in the queue and waiting to run. If a user logs off while their job is transferring, the job transitions to the queued state.


### -field BG_JOB_STATE_CONNECTING

Specifies that BITS is trying to connect to the server. If the connection succeeds, the state of the job becomes <b>BG_JOB_STATE_TRANSFERRING</b>; otherwise, the state becomes <b>BG_JOB_STATE_TRANSIENT_ERROR</b>.


### -field BG_JOB_STATE_TRANSFERRING

Specifies that BITS is transferring data for the job.


### -field BG_JOB_STATE_SUSPENDED

Specifies that the job is suspended (paused). To suspend a job, call the 
<a href="https://msdn.microsoft.com/88429730-b8e5-4969-934c-f0945fdd46a6">IBackgroundCopyJob::Suspend</a> method. BITS automatically suspends a job when it is created. The job remains suspended until you call the <a href="https://msdn.microsoft.com/a9e6f057-0a51-4f2d-810b-edbb3e019370">IBackgroundCopyJob::Resume</a>, <a href="https://msdn.microsoft.com/d57b0b2e-1181-45ed-b7fc-d002d14527cf">IBackgroundCopyJob::Complete</a>, or <a href="https://msdn.microsoft.com/bb3f32d9-298a-4099-8d87-4057ddefb0ba">IBackgroundCopyJob::Cancel</a> method.


### -field BG_JOB_STATE_ERROR

Specifies that a nonrecoverable error occurred (the service is unable to transfer the file). If the error, such as an access-denied error, can be corrected, call the 
<a href="https://msdn.microsoft.com/a9e6f057-0a51-4f2d-810b-edbb3e019370">IBackgroundCopyJob::Resume</a> method after the error is fixed. However, if the error cannot be corrected, call the 
<a href="https://msdn.microsoft.com/bb3f32d9-298a-4099-8d87-4057ddefb0ba">IBackgroundCopyJob::Cancel</a> method to cancel the job, or call the 
<a href="https://msdn.microsoft.com/d57b0b2e-1181-45ed-b7fc-d002d14527cf">IBackgroundCopyJob::Complete</a> method to accept the portion of a download job that transferred successfully.


### -field BG_JOB_STATE_TRANSIENT_ERROR

Specifies that a recoverable error occurred. BITS will retry jobs in the transient error state based on the retry interval you specify (see <a href="https://msdn.microsoft.com/52d2b7a1-6f68-424e-9c0b-a9f8df4a5ad6">IBackgroundCopyJob::SetMinimumRetryDelay</a>). The state of the job changes to <b>BG_JOB_STATE_ERROR</b> if the job fails to make progress (see  <a href="https://msdn.microsoft.com/3fcf46ed-197f-46ad-ac62-2c4a2e8b27ef">IBackgroundCopyJob::SetNoProgressTimeout</a>).

BITS does not retry the job if a network disconnect or disk lock error occurred (for example, chkdsk is running) or the <a href="https://msdn.microsoft.com/32c7e2b1-bac2-4708-a30c-f6b2a816c1a4">MaxInternetBandwidth</a> Group Policy is zero. 


### -field BG_JOB_STATE_TRANSFERRED

Specifies that your job was successfully processed. You must call the 
<a href="https://msdn.microsoft.com/d57b0b2e-1181-45ed-b7fc-d002d14527cf">IBackgroundCopyJob::Complete</a> method to acknowledge completion of the job and to make the files available to the client.


### -field BG_JOB_STATE_ACKNOWLEDGED

Specifies that you called the <a href="https://msdn.microsoft.com/d57b0b2e-1181-45ed-b7fc-d002d14527cf">IBackgroundCopyJob::Complete</a> method to acknowledge that your job completed successfully.


### -field BG_JOB_STATE_CANCELLED

Specifies that you called the 
<a href="https://msdn.microsoft.com/bb3f32d9-298a-4099-8d87-4057ddefb0ba">IBackgroundCopyJob::Cancel</a> method to cancel the job (remove the job from the transfer queue).


## -see-also




<a href="https://msdn.microsoft.com/32789bd2-2368-473b-accf-ac6e317d0172">IBackgroundCopyJob::GetState</a>
 

 

