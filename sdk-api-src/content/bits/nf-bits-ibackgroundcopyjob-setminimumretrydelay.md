---
UID: NF:bits.IBackgroundCopyJob.SetMinimumRetryDelay
title: IBackgroundCopyJob::SetMinimumRetryDelay (bits.h)
description: Sets the minimum length of time that BITS waits after encountering a transient error condition before trying to transfer the file.
helpviewer_keywords: ["IBackgroundCopyJob interface [BITS]","SetMinimumRetryDelay method","IBackgroundCopyJob.SetMinimumRetryDelay","IBackgroundCopyJob::SetMinimumRetryDelay","SetMinimumRetryDelay","SetMinimumRetryDelay method [BITS]","SetMinimumRetryDelay method [BITS]","IBackgroundCopyJob interface","_drz_ibackgroundcopyjob_setminimumretrydelay","bits.ibackgroundcopyjob_setminimumretrydelay","bits/IBackgroundCopyJob::SetMinimumRetryDelay"]
old-location: bits\ibackgroundcopyjob_setminimumretrydelay.htm
tech.root: Bits
ms.assetid: 52d2b7a1-6f68-424e-9c0b-a9f8df4a5ad6
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyJob interface [BITS],SetMinimumRetryDelay method, IBackgroundCopyJob.SetMinimumRetryDelay, IBackgroundCopyJob::SetMinimumRetryDelay, SetMinimumRetryDelay, SetMinimumRetryDelay method [BITS], SetMinimumRetryDelay method [BITS],IBackgroundCopyJob interface, _drz_ibackgroundcopyjob_setminimumretrydelay, bits.ibackgroundcopyjob_setminimumretrydelay, bits/IBackgroundCopyJob::SetMinimumRetryDelay
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
 - IBackgroundCopyJob::SetMinimumRetryDelay
 - bits/IBackgroundCopyJob::SetMinimumRetryDelay
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
 - IBackgroundCopyJob.SetMinimumRetryDelay
---

# IBackgroundCopyJob::SetMinimumRetryDelay


## -description

Sets the minimum length of time that BITS waits after encountering a transient error condition before trying to transfer the file.

## -parameters

### -param Seconds [in]

Minimum length of time, in seconds, that BITS waits after encountering a transient error before trying to transfer the file. The default retry delay is 600 seconds (10 minutes). The minimum retry delay that you can specify is 5 seconds. If you specify a value less than 5 seconds, BITS changes the value to 5 seconds. If the value exceeds the no-progress-timeout 
value retrieved from the <a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-getprogress">GetNoProgressTimeout</a> method, BITS will not retry the transfer and moves the job to the BG_JOB_STATE_ERROR state.

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
Retry delay was successfully set.

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

To start the job before the minimum retry period expires, call the <a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-resume">IBackgroundCopyJob::Resume</a>  method.

BITS does not retry the job if a network disconnect or disk lock error occurred (for example, chkdsk is running) or the <a href="/windows/desktop/Bits/group-policies">MaxInternetBandwidth</a> Group Policy is zero. 

<b>Note</b>  Changing the system clock does not affect the minimum retry delay. For example, if the current time is 2:00 P.M. and BITS is to retry the job at 2:10 P.M.,  moving the system clock forward ten or more minutes does not mean BITS  will retry the job  early—BITS will still retry the job in ten minutes. To reflect the system clock change in BITS, you must restart the computer or the BITS service.

## -see-also

<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-getminimumretrydelay">IBackgroundCopyJob::GetMinimumRetryDelay</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-getnoprogresstimeout">IBackgroundCopyJob::GetNoProgressTimeout</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout">IBackgroundCopyJob::SetNoProgressTimeout</a>