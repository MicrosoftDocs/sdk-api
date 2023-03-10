---
UID: NF:bits.IBackgroundCopyCallback.JobTransferred
title: IBackgroundCopyCallback::JobTransferred (bits.h)
description: BITS calls your implementation of the JobTransferred method when all of the files in the job have been successfully transferred.
helpviewer_keywords: ["IBackgroundCopyCallback interface [BITS]","JobTransferred method","IBackgroundCopyCallback.JobTransferred","IBackgroundCopyCallback::JobTransferred","JobTransferred","JobTransferred method [BITS]","JobTransferred method [BITS]","IBackgroundCopyCallback interface","_drz_ibackgroundcopycallback_jobtransferred","bits.ibackgroundcopycallback_jobtransferred","bits/IBackgroundCopyCallback::JobTransferred"]
old-location: bits\ibackgroundcopycallback_jobtransferred.htm
tech.root: Bits
ms.assetid: 04ff96c4-5b22-4935-bce8-5b9d3196cbe5
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyCallback interface [BITS],JobTransferred method, IBackgroundCopyCallback.JobTransferred, IBackgroundCopyCallback::JobTransferred, JobTransferred, JobTransferred method [BITS], JobTransferred method [BITS],IBackgroundCopyCallback interface, _drz_ibackgroundcopycallback_jobtransferred, bits.ibackgroundcopycallback_jobtransferred, bits/IBackgroundCopyCallback::JobTransferred
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
 - IBackgroundCopyCallback::JobTransferred
 - bits/IBackgroundCopyCallback::JobTransferred
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
 - IBackgroundCopyCallback.JobTransferred
---

# IBackgroundCopyCallback::JobTransferred


## -description

BITS calls your implementation of the 
<b>JobTransferred</b> method when all of the files in the job have been successfully transferred. For BG_JOB_TYPE_UPLOAD_REPLY jobs, BITS calls the 
<b>JobTransferred</b> method after the upload file has been transferred to the server and the reply has been transferred to the client.

## -parameters

### -param pJob [in]

Contains job-related information, such as the time the job completed, the number of bytes transferred, and the number of files transferred. Do not release <i>pJob</i>; BITS releases the interface when the method returns.

## -returns

This method should return <b>S_OK</b>; otherwise,  BITS continues to call this method until <b>S_OK</b> is returned. For performance reasons, you should limit the number  of times you return a value other than <b>S_OK</b> to a few times. As an alternative to returning an error code, consider always returning <b>S_OK</b> and handling the error internally. The interval at which this method is called is arbitrary.

Note that if this method fails and you   called the <a href="/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline">IBackgroundCopyJob2::SetNotifyCmdLine</a> method, the command line is executed and this method is not called again.

## -remarks

Typically, your implementation should call the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-complete">IBackgroundCopyJob::Complete</a> method to acknowledge that BITS successfully transferred the files. Download files and the reply file are not available on the client until you call the 
<b>Complete</b> method.

If you do not call the <a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-complete">Complete</a> method or the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-cancel">IBackgroundCopyJob::Cancel</a> method within 90 days (default <a href="/windows/desktop/Bits/group-policies">JobInactivityTimeout</a> Group Policy), BITS cancels the job and deletes the downloaded files and reply file; job cancellation does not affect files that have been successfully uploaded.

If you want to retrieve the reply data in your callback, query <i>pJob</i> for the 
<a href="/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2">IBackgroundCopyJob2</a> interface and call its 
<a href="/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata">GetReplyData</a> method. To retrieve the name of the file that contains the reply data, call the 
<a href="/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename">GetReplyFileName</a> method.

BITS does not guarantee the integrity of the transferred files against third-party intrusions. Clients can implement integrity checks to validate transferred files before calling the <a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-complete">Complete</a>  method. To get notification when a file is transferred, implement the <a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibackgroundcopycallback2-filetransferred">IBackgroundCopyCallback2::FileTransferred</a> method. Inside the callback, call the <a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname">IBackgroundCopyFile3::GetTemporaryName</a> method to get the name of the temporary file that contains the downloaded content. Validate the contents and then call the <a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate">IBackgroundCopyFile3::SetValidationState</a> method to indicate if the content is valid. If the content is not valid and BITS downloaded the file from the origin server, the job goes in the error state. If the job was downloaded from a peer, BITS downloads the file from the origin server.

<div class="alert"><b>Note</b>  BITS supports up to four simultaneous notifications per user. If one or more applications  block all four notifications for a user from returning, an application running as the same user will not receive  notifications until one or more of the blocking notifications return. To reduce the chance that your callback blocks other notifications, keep your implementation short.</div>
<div> </div>

#### Examples

See the example code for the 
<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopycallback">IBackgroundCopyCallback</a> interface.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopycallback">IBackgroundCopyCallback</a>



<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyjob">IBackgroundCopyJob</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-cancel">IBackgroundCopyJob::Cancel</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-complete">IBackgroundCopyJob::Complete</a>