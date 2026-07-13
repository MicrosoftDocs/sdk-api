---
UID: NF:bits.IBackgroundCopyJob.Cancel
title: IBackgroundCopyJob::Cancel (bits.h)
description: Deletes the job from the transfer queue and removes related temporary files from the client (downloads) and server (uploads).
helpviewer_keywords: ["Cancel","Cancel method [BITS]","Cancel method [BITS]","IBackgroundCopyJob interface","IBackgroundCopyJob interface [BITS]","Cancel method","IBackgroundCopyJob.Cancel","IBackgroundCopyJob::Cancel","_drz_ibackgroundcopyjob_cancel","bits.ibackgroundcopyjob_cancel","bits/IBackgroundCopyJob::Cancel"]
old-location: bits\ibackgroundcopyjob_cancel.htm
tech.root: Bits
ms.assetid: bb3f32d9-298a-4099-8d87-4057ddefb0ba
ms.date: 12/05/2018
ms.keywords: Cancel, Cancel method [BITS], Cancel method [BITS],IBackgroundCopyJob interface, IBackgroundCopyJob interface [BITS],Cancel method, IBackgroundCopyJob.Cancel, IBackgroundCopyJob::Cancel, _drz_ibackgroundcopyjob_cancel, bits.ibackgroundcopyjob_cancel, bits/IBackgroundCopyJob::Cancel
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
 - IBackgroundCopyJob::Cancel
 - bits/IBackgroundCopyJob::Cancel
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
 - IBackgroundCopyJob.Cancel
---

# IBackgroundCopyJob::Cancel


## -description

Deletes the job from the transfer queue and removes related temporary files from the client (downloads) and server (uploads).



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
Job was successfully canceled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_S_UNABLE_TO_DELETE_FILES</b></dt>
</dl>
</td>
<td width="60%">
Job was successfully canceled; however, the service was unable to delete the temporary files associated with the job.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
Cannot cancel a job whose state is BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.

</td>
</tr>
</table>

## -remarks

You can 
<a href="/windows/desktop/Bits/completing-and-canceling-a-job">cancel a job</a> at any time; however, the job cannot be recovered after it is canceled.

For upload jobs, if the server is unavailable, there may be a delay before BITS deletes the job from the queue. BITS periodically sends a cancel request to the BITS server for up to 24 hours. If the server does not respond within the 24-hour period, BITS removes the job from the queue. If the <a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout">no-progress time-out period</a> is less than 24 hours, BITS uses the no-progress time-out period to limit the retries.

The 
<b>Cancel</b> method cancels an upload if the upload is not complete. If the upload is complete and the job is of type BG_JOB_TYPE_UPLOAD_REPLY, the method cancels the reply.

## -see-also

<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-complete">IBackgroundCopyJob::Complete</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-resume">IBackgroundCopyJob::Resume</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-suspend">IBackgroundCopyJob::Suspend</a>
