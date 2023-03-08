---
UID: NE:bits.BG_JOB_STATE
title: BG_JOB_STATE (bits.h)
description: Defines constants that specify the different states of a job.
helpviewer_keywords: ["BG_JOB_STATE","BG_JOB_STATE enumeration [BITS]","BG_JOB_STATE_ACKNOWLEDGED","BG_JOB_STATE_CANCELLED","BG_JOB_STATE_CONNECTING","BG_JOB_STATE_ERROR","BG_JOB_STATE_QUEUED","BG_JOB_STATE_SUSPENDED","BG_JOB_STATE_TRANSFERRED","BG_JOB_STATE_TRANSFERRING","BG_JOB_STATE_TRANSIENT_ERROR","_drz_bg_job_state","bits.bg_job_state","bits/BG_JOB_STATE","bits/BG_JOB_STATE_ACKNOWLEDGED","bits/BG_JOB_STATE_CANCELLED","bits/BG_JOB_STATE_CONNECTING","bits/BG_JOB_STATE_ERROR","bits/BG_JOB_STATE_QUEUED","bits/BG_JOB_STATE_SUSPENDED","bits/BG_JOB_STATE_TRANSFERRED","bits/BG_JOB_STATE_TRANSFERRING","bits/BG_JOB_STATE_TRANSIENT_ERROR"]
old-location: bits\bg_job_state.htm
tech.root: Bits
ms.assetid: a7857cf1-05b7-42df-b79e-50a2f6a406dc
ms.date: 02/22/2019
ms.keywords: BG_JOB_STATE, BG_JOB_STATE enumeration [BITS], BG_JOB_STATE_ACKNOWLEDGED, BG_JOB_STATE_CANCELLED, BG_JOB_STATE_CONNECTING, BG_JOB_STATE_ERROR, BG_JOB_STATE_QUEUED, BG_JOB_STATE_SUSPENDED, BG_JOB_STATE_TRANSFERRED, BG_JOB_STATE_TRANSFERRING, BG_JOB_STATE_TRANSIENT_ERROR, _drz_bg_job_state, bits.bg_job_state, bits/BG_JOB_STATE, bits/BG_JOB_STATE_ACKNOWLEDGED, bits/BG_JOB_STATE_CANCELLED, bits/BG_JOB_STATE_CONNECTING, bits/BG_JOB_STATE_ERROR, bits/BG_JOB_STATE_QUEUED, bits/BG_JOB_STATE_SUSPENDED, bits/BG_JOB_STATE_TRANSFERRED, bits/BG_JOB_STATE_TRANSFERRING, bits/BG_JOB_STATE_TRANSIENT_ERROR
req.header: bits.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: BG_JOB_STATE
req.redist: 
f1_keywords:
 - BG_JOB_STATE
 - bits/BG_JOB_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bits.h
api_name:
 - BG_JOB_STATE
---

# BG_JOB_STATE enumeration


## -description

Defines constants that specify the different states of a job.

## -enum-fields

### -field BG_JOB_STATE_QUEUED:0

Specifies that the job is in the queue, and waiting to run. If a user logs off while their job is transferring, the job transitions to the queued state.

### -field BG_JOB_STATE_CONNECTING

Specifies that BITS is trying to connect to the server. If the connection succeeds, the state of the job becomes <strong>BG_JOB_STATE_TRANSFERRING</strong>; otherwise, the state becomes <strong>BG_JOB_STATE_TRANSIENT_ERROR</strong>.

### -field BG_JOB_STATE_TRANSFERRING

Specifies that BITS is transferring data for the job.

### -field BG_JOB_STATE_SUSPENDED

Specifies that the job is suspended (paused). To suspend a job, call the <a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-suspend">IBackgroundCopyJob::Suspend method</a>. BITS automatically suspends a job when it is created. The job remains suspended until you call the <a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-resume">IBackgroundCopyJob::Resume method</a>, <a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-complete">IBackgroundCopyJob::Complete method</a>, or <a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-cancel">IBackgroundCopyJob::Cancel method</a>.

### -field BG_JOB_STATE_ERROR

Specifies that a nonrecoverable error occurred (the service is unable to transfer the file). If the error&mdash;such as an access-denied error&mdash;can be corrected, then call the 
[IBackgroundCopyJob::Resume method](/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-resume)<a href=""></a> after the error is fixed. However, if the error cannot be corrected, then call the 
[IBackgroundCopyJob::Cancel method](/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-cancel)<a href=""></a> to cancel the job, or call the 
[IBackgroundCopyJob::Complete method](/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-complete)<a href=""></a> to accept the portion of a download job that transferred successfully.

### -field BG_JOB_STATE_TRANSIENT_ERROR

Specifies that a recoverable error occurred. BITS will retry jobs in the transient error state based on the retry interval you specify (see [IBackgroundCopyJob::SetMinimumRetryDelay method](/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay)<a href=""></a>). The state of the job changes to <strong>BG_JOB_STATE_ERROR</strong> if the job fails to make progress (see [IBackgroundCopyJob::SetNoProgressTimeout method](/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout)<a href=""></a>).

BITS does not retry the job if a network disconnect or a disk lock error occurred (for example, `chkdsk` is running), or the [MaxInternetBandwidth](/windows/desktop/Bits/group-policies)<a href=""></a> Group Policy is zero.

### -field BG_JOB_STATE_TRANSFERRED

Specifies that your job was successfully processed. You must call the 
[IBackgroundCopyJob::Complete method](/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-complete)<a href=""></a> to acknowledge completion of the job, and to make the files available to the client.

### -field BG_JOB_STATE_ACKNOWLEDGED

Specifies that you called the [IBackgroundCopyJob::Complete method](/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-complete)<a href=""></a> to acknowledge that your job completed successfully.

### -field BG_JOB_STATE_CANCELLED

Specifies that you called the 
[IBackgroundCopyJob::Cancel method](/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-cancel)<a href=""></a> to cancel the job (that is, to remove the job from the transfer queue).

## -see-also

* [IBackgroundCopyJob::GetState method](/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-getstate)
