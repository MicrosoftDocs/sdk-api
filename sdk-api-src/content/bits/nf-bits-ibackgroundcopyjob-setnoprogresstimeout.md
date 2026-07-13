---
UID: NF:bits.IBackgroundCopyJob.SetNoProgressTimeout
title: IBackgroundCopyJob::SetNoProgressTimeout (bits.h)
description: Sets the length of time that BITS tries to transfer the file after a transient error condition occurs. If there is progress, the timer is reset.
helpviewer_keywords: ["IBackgroundCopyJob interface [BITS]","SetNoProgressTimeout method","IBackgroundCopyJob.SetNoProgressTimeout","IBackgroundCopyJob::SetNoProgressTimeout","SetNoProgressTimeout","SetNoProgressTimeout method [BITS]","SetNoProgressTimeout method [BITS]","IBackgroundCopyJob interface","_drz_ibackgroundcopyjob_setnoprogresstimeout","bits.ibackgroundcopyjob_setnoprogresstimeout","bits/IBackgroundCopyJob::SetNoProgressTimeout"]
old-location: bits\ibackgroundcopyjob_setnoprogresstimeout.htm
tech.root: Bits
ms.assetid: 3fcf46ed-197f-46ad-ac62-2c4a2e8b27ef
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyJob interface [BITS],SetNoProgressTimeout method, IBackgroundCopyJob.SetNoProgressTimeout, IBackgroundCopyJob::SetNoProgressTimeout, SetNoProgressTimeout, SetNoProgressTimeout method [BITS], SetNoProgressTimeout method [BITS],IBackgroundCopyJob interface, _drz_ibackgroundcopyjob_setnoprogresstimeout, bits.ibackgroundcopyjob_setnoprogresstimeout, bits/IBackgroundCopyJob::SetNoProgressTimeout
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
 - IBackgroundCopyJob::SetNoProgressTimeout
 - bits/IBackgroundCopyJob::SetNoProgressTimeout
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
 - IBackgroundCopyJob.SetNoProgressTimeout
---

# IBackgroundCopyJob::SetNoProgressTimeout


## -description

Sets the length of time that BITS tries to transfer the file after a transient error condition occurs. If there is progress, the timer is reset.

## -parameters

### -param Seconds [in]

Length of time, in seconds, that BITS tries to transfer the file after the first transient error occurs. The default retry period is 1,209,600 seconds (14 days). Set the retry period to 0 to prevent retries and to force the job into the BG_JOB_STATE_ERROR state for all errors. If the retry period value exceeds the <a href="/windows/desktop/Bits/group-policies">JobInactivityTimeout</a> Group Policy value (90-day default), BITS cancels the job after the policy value is exceeded.

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
Retry period successfully set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.

</td>
</tr>
</table>

## -remarks

If BITS does not make progress during the retry period, it moves the state of the job from BG_JOB_STATE_TRANSIENT_ERROR to BG_JOB_STATE_ERROR. If you request error notification, BITS then calls your 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopycallback-joberror">JobError</a> callback.

<b>Note</b>  Changing the system clock does not affect the retry period. For example, if the retry period expires in 14 days, moving the system clock forward 14 or more days does not mean the retry period expires early—the retry period will still expire in 14 days. To reflect the system clock change in BITS, you must restart the computer or the BITS service.

## -see-also

<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-getnoprogresstimeout">IBackgroundCopyJob::GetNoProgressTimeout</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay">IBackgroundCopyJob::SetMinimumRetryDelay</a>