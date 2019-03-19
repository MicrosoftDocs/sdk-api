---
UID: NF:bits.IBackgroundCopyJob.GetError
title: IBackgroundCopyJob::GetError (bits.h)
author: windows-sdk-content
description: Retrieves the error interface after an error occurs.
old-location: bits\ibackgroundcopyjob_geterror.htm
tech.root: Bits
ms.assetid: 2ad4c913-2d1e-4490-968c-960178a57e3b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetError, GetError method [BITS], GetError method [BITS],IBackgroundCopyJob interface, IBackgroundCopyJob interface [BITS],GetError method, IBackgroundCopyJob.GetError, IBackgroundCopyJob::GetError, _drz_ibackgroundcopyjob_geterror, bits.ibackgroundcopyjob_geterror, bits/IBackgroundCopyJob::GetError
ms.topic: method
req.header: bits.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyJob.GetError
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBackgroundCopyJob::GetError


## -description


Retrieves the error interface after an error occurs.

BITS generates an error object when the state of the job is 
<a href="https://msdn.microsoft.com/a7857cf1-05b7-42df-b79e-50a2f6a406dc">BG_JOB_STATE_ERROR</a> or BG_JOB_STATE_TRANSIENT_ERROR. The service does not create an error object when a call to an <b>IBackgroundCopyXXXX</b> interface method fails. The error object is available until BITS begins transferring data (the state of the job changes to BG_JOB_STATE_TRANSFERRING) for the job or until your application exits.


## -parameters




### -param ppError [out]

Error interface that provides the error code, a description of the error, and the context in which the error occurred. This parameter also  identifies the file being transferred at the time the error occurred. Release <i>ppError</i> when done.


## -returns



This method returns the following <b>HRESULT</b> values, as well as others.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
Successfully generated the error object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_ERROR_INFORMATION_UNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The error interface is available only after an error occurs (BG_JOB_STATE_ERROR or BG_JOB_STATE_TRANSIENT_ERROR) and before BITS begins transferring data (BG_JOB_STATE_TRANSFERRING).

</td>
</tr>
</table>
 




## -remarks



The job is placed in an error state on fatal errors or after the 
no-progress-timeout  period expires for transient errors (this period is retrieved from the <a href="https://msdn.microsoft.com/30aae990-1cc1-468b-9e5f-7ef5ce6eeb9a">GetNoProgressTimeout</a> method). Use one of the following options to determine if the job is in error:

<ul>
<li>To poll for the state of the job, call the 
<a href="https://msdn.microsoft.com/32789bd2-2368-473b-accf-ac6e317d0172">IBackgroundCopyJob::GetState</a> method. The job is in error if the state is BG_JOB_STATE_ERROR.</li>
<li>To receive notification when an error occurs, implement the 
<a href="https://msdn.microsoft.com/e1aa6775-d1e5-4463-ae0f-32c0498881e1">IBackgroundCopyCallback</a> interface (specifically, the 
<a href="https://msdn.microsoft.com/3e206195-1a8c-435e-9b8f-6517b8e3c4ca">JobError</a> method). Then, call the 
<a href="https://msdn.microsoft.com/34d51546-ec27-471f-9da5-3bec7ed4e1ea">IBackgroundCopyJob::SetNotifyInterface</a> method to register the callback and the 
<a href="https://msdn.microsoft.com/24aa6445-d7bd-4825-9121-402e63ae6f69">IBackgroundCopyJob::SetNotifyFlags</a> method to set the BG_NOTIFY_JOB_ERROR flag.</li>
</ul>
The 
<a href="https://msdn.microsoft.com/a0b9e887-84d5-4f67-a65c-6a807c50dafd">IBackgroundCopyError</a> interface contains information that you use to determine the cause of the error and if the transfer process can proceed. After you determine the cause of the error, perform one of the following options:

<ul>
<li>To cancel the job, call the 
<a href="https://msdn.microsoft.com/bb3f32d9-298a-4099-8d87-4057ddefb0ba">IBackgroundCopyJob::Cancel</a> method.</li>
<li>To save those files that transferred successfully before the error occurred, call the 
<a href="https://msdn.microsoft.com/d57b0b2e-1181-45ed-b7fc-d002d14527cf">IBackgroundCopyJob::Complete</a> method.</li>
<li>To finish processing the job, fix the problem, and then call the 
<a href="https://msdn.microsoft.com/a9e6f057-0a51-4f2d-810b-edbb3e019370">IBackgroundCopyJob::Resume</a> method.</li>
</ul>
If the job remains in an error state for 90 days (default <a href="https://msdn.microsoft.com/32c7e2b1-bac2-4708-a30c-f6b2a816c1a4">JobInactivityTimeout</a> Group Policy), the service removes the job from the queue and deletes the temporary files on the client; job deletion does not affect files that have been successfully uploaded.

To determine whether the upload, reply, or server application portion of an upload-reply job failed, call the 
<a href="https://msdn.microsoft.com/abdf115d-3ff2-4664-b053-f55872ad24ab">IBackgroundCopyError::GetError</a> method to retrieve the 
<a href="https://msdn.microsoft.com/c9d98518-6f2e-4fd1-b0ee-6735c6d6ecd9">context</a> in which the error occurred. The server application failed if the context is BG_ERROR_CONTEXT_REMOTE_APPLICATION. If the error is with the upload or reply, the context is BG_ERROR_CONTEXT_REMOTE_FILE. The upload failed if the <b>BytesTotal</b> member of the 
<a href="https://msdn.microsoft.com/ea78ee22-87b2-4859-bd49-dd309c8aa234">BG_JOB_REPLY_PROGRESS</a> structure is BG_SIZE_UNKNOWN. Otherwise, the reply failed.


#### Examples

See the example code in the 
<a href="https://msdn.microsoft.com/cbc182ce-c853-492e-8953-21c54500875b">Handling Errors</a>  topic.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/3e206195-1a8c-435e-9b8f-6517b8e3c4ca">IBackgroundCopyCallback::JobError</a>



<a href="https://msdn.microsoft.com/a0b9e887-84d5-4f67-a65c-6a807c50dafd">IBackgroundCopyError</a>



<a href="https://msdn.microsoft.com/32789bd2-2368-473b-accf-ac6e317d0172">IBackgroundCopyJob::GetState</a>
 

 

