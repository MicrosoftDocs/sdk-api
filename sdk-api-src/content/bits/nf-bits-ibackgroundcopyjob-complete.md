---
UID: NF:bits.IBackgroundCopyJob.Complete
title: IBackgroundCopyJob::Complete (bits.h)
description: Ends the job and saves the transferred files on the client.
helpviewer_keywords: ["Complete","Complete method [BITS]","Complete method [BITS]","IBackgroundCopyJob interface","IBackgroundCopyJob interface [BITS]","Complete method","IBackgroundCopyJob.Complete","IBackgroundCopyJob::Complete","_drz_ibackgroundcopyjob_complete","bits.ibackgroundcopyjob_complete","bits/IBackgroundCopyJob::Complete"]
old-location: bits\ibackgroundcopyjob_complete.htm
tech.root: Bits
ms.assetid: d57b0b2e-1181-45ed-b7fc-d002d14527cf
ms.date: 12/05/2018
ms.keywords: Complete, Complete method [BITS], Complete method [BITS],IBackgroundCopyJob interface, IBackgroundCopyJob interface [BITS],Complete method, IBackgroundCopyJob.Complete, IBackgroundCopyJob::Complete, _drz_ibackgroundcopyjob_complete, bits.ibackgroundcopyjob_complete, bits/IBackgroundCopyJob::Complete
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
 - IBackgroundCopyJob::Complete
 - bits/IBackgroundCopyJob::Complete
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
 - IBackgroundCopyJob.Complete
---

# IBackgroundCopyJob::Complete


## -description

Ends the job and saves the transferred files on the client.



## -returns

This method returns the following <b>HRESULT</b> values. The method can also return errors related to renaming the temporary copies of the transferred files to their given names.

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
All files transferred successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_S_PARTIAL_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
A subset of the files transferred successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_S_UNABLE_TO_DELETE_FILES</b></dt>
</dl>
</td>
<td width="60%">
Job was successfully completed; however, the service was unable to delete the temporary files associated with the job.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
For downloads, the state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED. 




For uploads, the state of the job must be BG_JOB_STATE_TRANSFERRED.

</td>
</tr>
</table>

## -remarks

Download files are not available until you call the 
<b>Complete</b> method. Call the 
<b>Complete</b> method after BITS successfully transfers the files. The 
method renames the temporary download files to their final destination names and removes the job from the queue. Note that BITS renames the temporary upload file when the server receives the last fragment, which is why  download jobs require network connectivity and upload jobs do not. 

All of the files have been successfully transferred if the job's state is <b>BG_JOB_STATE_TRANSFERRED</b>. To check the state of the job, call the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-getstate">IBackgroundCopyJob::GetState</a> method. You can also implement the 
<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopycallback">IBackgroundCopyCallback</a> interface to receive notification when all of the files have been transferred to the client. 

If you do not call the 
<b>Complete</b> method or the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-cancel">IBackgroundCopyJob::Cancel</a> method within 90 days (default <a href="/windows/desktop/Bits/group-policies">JobInactivityTimeout</a> Group Policy), the service cancels the job. If the service cancels the job, the downloaded files and the reply file are not available to the client; job cancellation does not affect files that have been successfully uploaded.

BITS removes the job from the transfer queue if the HRESULT is <b>S_OK</b> or BG_S_PARTIAL_COMPLETE. The job remains in the transfer queue if BITS was unable to rename all of the temporary files. Files that were renamed successfully are available to the user. The job remains in the queue (the state is <b>BG_JOB_STATE_TRANSFERRED</b>) until the application is able to fix the problem and calls either the 
<b>Complete</b> method again or the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-cancel">IBackgroundCopyJob::Cancel</a> method to cancel the job. To determine which files were not renamed for download jobs, see the <b>Completed</b> member of the 
<a href="/windows/desktop/api/bits/ns-bits-bg_file_progress">BG_FILE_PROGRESS</a> structure. 

For download jobs, you can call the 
<b>Complete</b> method at anytime during the transfer process; however, only files that were successfully transferred to the client before calling this method are saved. For example, if you call the 
<b>Complete</b> method while BITS is processing the third of five files, only the first two files are saved. To determine which files have been transferred, call the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyfile-getprogress">IBackgroundCopyFile::GetProgress</a> method and compare the <b>BytesTransferred</b> member to the <b>BytesTotal</b> member of the 
<a href="/windows/desktop/api/bits/ns-bits-bg_file_progress">BG_FILE_PROGRESS</a> structure.

For upload jobs, you can call the 
<b>Complete</b> method only when the job's state is <b>BG_JOB_STATE_TRANSFERRED</b>.

BITS does not guarantee the integrity of the transferred files against third-party intrusions. Clients can implement integrity checks to validate transferred files after calling the 
<b>Complete</b> method.

The owner of the file is the user who made the call. For example, if an administrator completes someone else's job, the administrator—not the owner of the job—owns the file.

<b>BITS 1.2 and earlier:  </b>The owner of the file is the owner of the job, regardless of who called the <b>Complete</b> method.

## -see-also

<a href="/windows/desktop/Bits/completing-and-canceling-a-job">Completing and Canceling a Job</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopycallback-jobtransferred">IBackgroundCopyCallback::JobTransferred</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-cancel">IBackgroundCopyJob::Cancel</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-getstate">IBackgroundCopyJob::GetState</a>
