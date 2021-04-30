---
UID: NF:bits.IBackgroundCopyCallback.JobError
title: IBackgroundCopyCallback::JobError (bits.h)
description: BITS calls your implementation of the JobError method when the state of the job changes to BG_JOB_STATE_ERROR.
helpviewer_keywords: ["IBackgroundCopyCallback interface [BITS]","JobError method","IBackgroundCopyCallback.JobError","IBackgroundCopyCallback::JobError","JobError","JobError method [BITS]","JobError method [BITS]","IBackgroundCopyCallback interface","_drz_ibackgroundcopycallback_joberror","bits.ibackgroundcopycallback_joberror","bits/IBackgroundCopyCallback::JobError"]
old-location: bits\ibackgroundcopycallback_joberror.htm
tech.root: Bits
ms.assetid: 3e206195-1a8c-435e-9b8f-6517b8e3c4ca
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyCallback interface [BITS],JobError method, IBackgroundCopyCallback.JobError, IBackgroundCopyCallback::JobError, JobError, JobError method [BITS], JobError method [BITS],IBackgroundCopyCallback interface, _drz_ibackgroundcopycallback_joberror, bits.ibackgroundcopycallback_joberror, bits/IBackgroundCopyCallback::JobError
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyCallback::JobError
 - bits/IBackgroundCopyCallback::JobError
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.h
api_name:
 - IBackgroundCopyCallback.JobError
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

Note that if this method fails and you   called the <a href="/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline">IBackgroundCopyJob2::SetNotifyCmdLine</a> method, the command line is executed and this method is not called again.

## -remarks

After you determine the cause of the error, perform one of the following options:

<ul>
<li>To cancel the job, call the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-cancel">IBackgroundCopyJob::Cancel</a>  method. The cancel request has no effect on upload jobs if the error occurred after the file was successfully uploaded. However, if the job type is BG_JOB_TYPE_UPLOAD_REPLY and the upload was successful, calling the 
<b>Cancel</b> method cancels the request for the reply data.</li>
<li>To accept the portion of the job that transferred successfully before the error occurred, call the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-complete">IBackgroundCopyJob::Complete</a> method. This option does not apply to upload jobs; you cannot complete a portion of an upload job.</li>
<li>To finish processing the job, fix the problem, and then call the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-resume">IBackgroundCopyJob::Resume</a> method.</li>
</ul>
If the job remains in an error state for 90 days (default <a href="/windows/desktop/Bits/group-policies">JobInactivityTimeout</a> Group Policy), BITS cancels the job and deletes related temporary files; job cancellation does not affect files that have been successfully uploaded.

Transient errors do not generate calls to the 
<b>JobError</b> method.

To determine whether the upload, reply, or server application portion of an upload reply job failed, call the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyerror-geterror">IBackgroundCopyError::GetError</a> method to retrieve the 
[context](./ne-bits-bg_error_context.md) in which the error occurred. The server application failed if the context is BG_ERROR_CONTEXT_REMOTE_APPLICATION. The context for upload and reply is BG_ERROR_CONTEXT_REMOTE_FILE. The reply failed if the <b>BytesTotal</b> member of the 
<a href="/windows/desktop/api/bits1_5/ns-bits1_5-bg_job_reply_progress">BG_JOB_REPLY_PROGRESS</a> structure is not BG_SIZE_UNKNOWN. Otherwise, the upload failed.

<div class="alert"><b>Note</b>  BITS supports up to four simultaneous notifications per user. If one or more applications  block all four notifications for a user from returning, an application running as the same user will not receive  notifications until one or more of the blocking notifications return. To reduce the chance that your callback blocks other notifications, keep your implementation short.</div>
<div> </div>

#### Examples

See the example code for the 
<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopycallback">IBackgroundCopyCallback</a> interface.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopycallback">IBackgroundCopyCallback</a>



<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyerror">IBackgroundCopyError</a>



<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyjob">IBackgroundCopyJob</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-cancel">IBackgroundCopyJob::Cancel</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-resume">IBackgroundCopyJob::Resume</a>