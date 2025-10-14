---
UID: NF:bits.IBackgroundCopyJob.GetError
title: IBackgroundCopyJob::GetError (bits.h)
description: Retrieves the error interface after an error occurs.
helpviewer_keywords: ["GetError","GetError method [BITS]","GetError method [BITS]","IBackgroundCopyJob interface","IBackgroundCopyJob interface [BITS]","GetError method","IBackgroundCopyJob.GetError","IBackgroundCopyJob::GetError","_drz_ibackgroundcopyjob_geterror","bits.ibackgroundcopyjob_geterror","bits/IBackgroundCopyJob::GetError"]
old-location: bits\ibackgroundcopyjob_geterror.htm
tech.root: Bits
ms.assetid: 2ad4c913-2d1e-4490-968c-960178a57e3b
ms.date: 12/05/2018
ms.keywords: GetError, GetError method [BITS], GetError method [BITS],IBackgroundCopyJob interface, IBackgroundCopyJob interface [BITS],GetError method, IBackgroundCopyJob.GetError, IBackgroundCopyJob::GetError, _drz_ibackgroundcopyjob_geterror, bits.ibackgroundcopyjob_geterror, bits/IBackgroundCopyJob::GetError
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyJob::GetError
 - bits/IBackgroundCopyJob::GetError
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyJob.GetError
---

# IBackgroundCopyJob::GetError


## -description

Retrieves the error interface after an error occurs.

BITS generates an error object when the state of the job is 
<a href="/windows/desktop/api/bits/ne-bits-bg_job_state">BG_JOB_STATE_ERROR</a> or BG_JOB_STATE_TRANSIENT_ERROR. The service does not create an error object when a call to an <b>IBackgroundCopyXXXX</b> interface method fails. The error object is available until BITS begins transferring data (the state of the job changes to BG_JOB_STATE_TRANSFERRING) for the job or until your application exits.

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
<dt><b>S_OK</b></dt>
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
no-progress-timeout  period expires for transient errors (this period is retrieved from the <a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-getprogress">GetNoProgressTimeout</a> method). Use one of the following options to determine if the job is in error:

<ul>
<li>To poll for the state of the job, call the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-getstate">IBackgroundCopyJob::GetState</a> method. The job is in error if the state is BG_JOB_STATE_ERROR.</li>
<li>To receive notification when an error occurs, implement the 
<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopycallback">IBackgroundCopyCallback</a> interface (specifically, the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopycallback-joberror">JobError</a> method). Then, call the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnotifyinterface">IBackgroundCopyJob::SetNotifyInterface</a> method to register the callback and the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnotifyflags">IBackgroundCopyJob::SetNotifyFlags</a> method to set the BG_NOTIFY_JOB_ERROR flag.</li>
</ul>
The 
<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyerror">IBackgroundCopyError</a> interface contains information that you use to determine the cause of the error and if the transfer process can proceed. After you determine the cause of the error, perform one of the following options:

<ul>
<li>To cancel the job, call the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-cancel">IBackgroundCopyJob::Cancel</a> method.</li>
<li>To save those files that transferred successfully before the error occurred, call the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-complete">IBackgroundCopyJob::Complete</a> method.</li>
<li>To finish processing the job, fix the problem, and then call the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-resume">IBackgroundCopyJob::Resume</a> method.</li>
</ul>
If the job remains in an error state for 90 days (default <a href="/windows/desktop/Bits/group-policies">JobInactivityTimeout</a> Group Policy), the service removes the job from the queue and deletes the temporary files on the client; job deletion does not affect files that have been successfully uploaded.

To determine whether the upload, reply, or server application portion of an upload-reply job failed, call the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyerror-geterror">IBackgroundCopyError::GetError</a> method to retrieve the 
[context](./ne-bits-bg_error_context.md) in which the error occurred. The server application failed if the context is BG_ERROR_CONTEXT_REMOTE_APPLICATION. If the error is with the upload or reply, the context is BG_ERROR_CONTEXT_REMOTE_FILE. The upload failed if the <b>BytesTotal</b> member of the 
<a href="/windows/desktop/api/bits1_5/ns-bits1_5-bg_job_reply_progress">BG_JOB_REPLY_PROGRESS</a> structure is BG_SIZE_UNKNOWN. Otherwise, the reply failed.


#### Examples

See the example code in the 
<a href="/windows/desktop/Bits/handling-errors">Handling Errors</a>  topic.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopycallback-joberror">IBackgroundCopyCallback::JobError</a>



<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyerror">IBackgroundCopyError</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-getstate">IBackgroundCopyJob::GetState</a>