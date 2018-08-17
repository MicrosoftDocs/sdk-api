---
UID: NF:bits.IBackgroundCopyCallback.JobError
title: IBackgroundCopyCallback::JobError
author: windows-sdk-content
description: BITS calls your implementation of the JobError method when the state of the job changes to BG_JOB_STATE_ERROR.
old-location: bits\ibackgroundcopycallback_joberror.htm
old-project: bits
ms.assetid: 3e206195-1a8c-435e-9b8f-6517b8e3c4ca
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IBackgroundCopyCallback interface [BITS],JobError method, IBackgroundCopyCallback.JobError, IBackgroundCopyCallback::JobError, JobError, JobError method [BITS], JobError method [BITS],IBackgroundCopyCallback interface, _drz_ibackgroundcopycallback_joberror, bits.ibackgroundcopycallback_joberror, bits/IBackgroundCopyCallback::JobError
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
 - Bits.h
api_name:
 - IBackgroundCopyCallback.JobError
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBackgroundCopyCallback::JobError


## -description


BITS calls your implementation of the 
<b>JobError</b> method when the state of the job changes to BG_JOB_STATE_ERROR.
		


## -parameters




### -param pJob [in]

Contains job-related information, such as the number of bytes and files transferred before the error occurred. It also contains the methods to resume and cancel the job. Do not release <i>pJob</i>; BITS releases the interface when the <b>JobError</b> method returns.


### -param pError [in]

Contains error information, such as the file being processed at the time the fatal error occurred and a description of the error. Do not release <i>pError</i>; BITS releases the interface when the <b>JobError</b> method returns.


## -returns



This method should return <b>S_OK</b>; otherwise,  BITS continues to call this method until <b>S_OK</b> is returned. For performance reasons, you should limit the number  of times you return a value other than <b>S_OK</b> to a few times. As an alternative to returning an error code, consider always returning <b>S_OK</b> and handling the error internally. The interval at which this method is called is arbitrary.

Note that if this method fails and you   called the <a href="https://msdn.microsoft.com/en-us/library/Aa362988(v=VS.85).aspx">IBackgroundCopyJob2::SetNotifyCmdLine</a> method, the command line is executed and this method is not called again.




## -remarks



After you determine the cause of the error, perform one of the following options:

<ul>
<li>To cancel the job, call the 
<a href="https://msdn.microsoft.com/en-us/library/Aa363020(v=VS.85).aspx">IBackgroundCopyJob::Cancel</a>  method. The cancel request has no effect on upload jobs if the error occurred after the file was successfully uploaded. However, if the job type is BG_JOB_TYPE_UPLOAD_REPLY and the upload was successful, calling the 
<b>Cancel</b> method cancels the request for the reply data.</li>
<li>To accept the portion of the job that transferred successfully before the error occurred, call the 
<a href="https://msdn.microsoft.com/en-us/library/Aa363021(v=VS.85).aspx">IBackgroundCopyJob::Complete</a> method. This option does not apply to upload jobs; you cannot complete a portion of an upload job.</li>
<li>To finish processing the job, fix the problem, and then call the 
<a href="https://msdn.microsoft.com/en-us/library/Aa363039(v=VS.85).aspx">IBackgroundCopyJob::Resume</a> method.</li>
</ul>
If the job remains in an error state for 90 days (default <a href="https://msdn.microsoft.com/en-us/library/Aa362844(v=VS.85).aspx">JobInactivityTimeout</a> Group Policy), BITS cancels the job and deletes related temporary files; job cancellation does not affect files that have been successfully uploaded.

Transient errors do not generate calls to the 
<b>JobError</b> method.

To determine whether the upload, reply, or server application portion of an upload reply job failed, call the 
<a href="https://msdn.microsoft.com/en-us/library/Aa362876(v=VS.85).aspx">IBackgroundCopyError::GetError</a> method to retrieve the 
<a href="https://msdn.microsoft.com/en-us/library/Aa362798(v=VS.85).aspx">context</a> in which the error occurred. The server application failed if the context is BG_ERROR_CONTEXT_REMOTE_APPLICATION. The context for upload and reply is BG_ERROR_CONTEXT_REMOTE_FILE. The reply failed if the <b>BytesTotal</b> member of the 
<a href="https://msdn.microsoft.com/en-us/library/Aa362808(v=VS.85).aspx">BG_JOB_REPLY_PROGRESS</a> structure is not BG_SIZE_UNKNOWN. Otherwise, the upload failed.

<div class="alert"><b>Note</b>  BITS supports up to four simultaneous notifications per user. If one or more applications  block all four notifications for a user from returning, an application running as the same user will not receive  notifications until one or more of the blocking notifications return. To reduce the chance that your callback blocks other notifications, keep your implementation short.</div>
<div> </div>

#### Examples

See the example code for the 
<a href="https://msdn.microsoft.com/en-us/library/Aa362867(v=VS.85).aspx">IBackgroundCopyCallback</a> interface.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa362867(v=VS.85).aspx">IBackgroundCopyCallback</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362875(v=VS.85).aspx">IBackgroundCopyError</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362973(v=VS.85).aspx">IBackgroundCopyJob</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa363020(v=VS.85).aspx">IBackgroundCopyJob::Cancel</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa363039(v=VS.85).aspx">IBackgroundCopyJob::Resume</a>
 

 

