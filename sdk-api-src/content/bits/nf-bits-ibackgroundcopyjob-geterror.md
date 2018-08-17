---
UID: NF:bits.IBackgroundCopyJob.GetError
title: IBackgroundCopyJob::GetError
author: windows-sdk-content
description: Retrieves the error interface after an error occurs.
old-location: bits\ibackgroundcopyjob_geterror.htm
old-project: bits
ms.assetid: 2ad4c913-2d1e-4490-968c-960178a57e3b
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetError, GetError method [BITS], GetError method [BITS],IBackgroundCopyJob interface, IBackgroundCopyJob interface [BITS],GetError method, IBackgroundCopyJob.GetError, IBackgroundCopyJob::GetError, _drz_ibackgroundcopyjob_geterror, bits.ibackgroundcopyjob_geterror, bits/IBackgroundCopyJob::GetError
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bits.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: BG_JOB_PROXY_USAGE
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
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
---

# IBackgroundCopyJob::GetError


## -description


Retrieves the error interface after an error occurs.

BITS generates an error object when the state of the job is 
<a href="https://msdn.microsoft.com/en-us/library/Aa362809(v=VS.85).aspx">BG_JOB_STATE_ERROR</a> or BG_JOB_STATE_TRANSIENT_ERROR. The service does not create an error object when a call to an <b>IBackgroundCopyXXXX</b> interface method fails. The error object is available until BITS begins transferring data (the state of the job changes to BG_JOB_STATE_TRANSFERRING) for the job or until your application exits.


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
no-progress-timeout  period expires for transient errors (this period is retrieved from the <a href="https://msdn.microsoft.com/en-us/library/Aa363034(v=VS.85).aspx">GetNoProgressTimeout</a> method). Use one of the following options to determine if the job is in error:

<ul>
<li>To poll for the state of the job, call the 
<a href="https://msdn.microsoft.com/en-us/library/Aa363036(v=VS.85).aspx">IBackgroundCopyJob::GetState</a> method. The job is in error if the state is BG_JOB_STATE_ERROR.</li>
<li>To receive notification when an error occurs, implement the 
<a href="https://msdn.microsoft.com/en-us/library/Aa362867(v=VS.85).aspx">IBackgroundCopyCallback</a> interface (specifically, the 
<a href="https://msdn.microsoft.com/en-us/library/Aa362872(v=VS.85).aspx">JobError</a> method). Then, call the 
<a href="https://msdn.microsoft.com/en-us/library/Aa363045(v=VS.85).aspx">IBackgroundCopyJob::SetNotifyInterface</a> method to register the callback and the 
<a href="https://msdn.microsoft.com/en-us/library/Aa363044(v=VS.85).aspx">IBackgroundCopyJob::SetNotifyFlags</a> method to set the BG_NOTIFY_JOB_ERROR flag.</li>
</ul>
The 
<a href="https://msdn.microsoft.com/en-us/library/Aa362875(v=VS.85).aspx">IBackgroundCopyError</a> interface contains information that you use to determine the cause of the error and if the transfer process can proceed. After you determine the cause of the error, perform one of the following options:

<ul>
<li>To cancel the job, call the 
<a href="https://msdn.microsoft.com/en-us/library/Aa363020(v=VS.85).aspx">IBackgroundCopyJob::Cancel</a> method.</li>
<li>To save those files that transferred successfully before the error occurred, call the 
<a href="https://msdn.microsoft.com/en-us/library/Aa363021(v=VS.85).aspx">IBackgroundCopyJob::Complete</a> method.</li>
<li>To finish processing the job, fix the problem, and then call the 
<a href="https://msdn.microsoft.com/en-us/library/Aa363039(v=VS.85).aspx">IBackgroundCopyJob::Resume</a> method.</li>
</ul>
If the job remains in an error state for 90 days (default <a href="https://msdn.microsoft.com/en-us/library/Aa362844(v=VS.85).aspx">JobInactivityTimeout</a> Group Policy), the service removes the job from the queue and deletes the temporary files on the client; job deletion does not affect files that have been successfully uploaded.

To determine whether the upload, reply, or server application portion of an upload-reply job failed, call the 
<a href="https://msdn.microsoft.com/en-us/library/Aa362876(v=VS.85).aspx">IBackgroundCopyError::GetError</a> method to retrieve the 
<a href="https://msdn.microsoft.com/en-us/library/Aa362798(v=VS.85).aspx">context</a> in which the error occurred. The server application failed if the context is BG_ERROR_CONTEXT_REMOTE_APPLICATION. If the error is with the upload or reply, the context is BG_ERROR_CONTEXT_REMOTE_FILE. The upload failed if the <b>BytesTotal</b> member of the 
<a href="https://msdn.microsoft.com/en-us/library/Aa362808(v=VS.85).aspx">BG_JOB_REPLY_PROGRESS</a> structure is BG_SIZE_UNKNOWN. Otherwise, the reply failed.


#### Examples

See the example code in the 
<a href="https://msdn.microsoft.com/en-us/library/Aa362845(v=VS.85).aspx">Handling Errors</a>  topic.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa362872(v=VS.85).aspx">IBackgroundCopyCallback::JobError</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362875(v=VS.85).aspx">IBackgroundCopyError</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa363036(v=VS.85).aspx">IBackgroundCopyJob::GetState</a>
 

 

