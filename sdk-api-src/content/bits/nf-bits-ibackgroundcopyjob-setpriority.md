---
UID: NF:bits.IBackgroundCopyJob.SetPriority
title: IBackgroundCopyJob::SetPriority (bits.h)
description: Specifies the priority level of your job. The priority level determines when your job is processed relative to other jobs in the transfer queue.
helpviewer_keywords: ["IBackgroundCopyJob interface [BITS]","SetPriority method","IBackgroundCopyJob.SetPriority","IBackgroundCopyJob::SetPriority","SetPriority","SetPriority method [BITS]","SetPriority method [BITS]","IBackgroundCopyJob interface","_drz_ibackgroundcopyjob_setpriority","bits.ibackgroundcopyjob_setpriority","bits/IBackgroundCopyJob::SetPriority"]
old-location: bits\ibackgroundcopyjob_setpriority.htm
tech.root: Bits
ms.assetid: 8b59128d-7e63-45dc-af0f-54ea844dac98
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyJob interface [BITS],SetPriority method, IBackgroundCopyJob.SetPriority, IBackgroundCopyJob::SetPriority, SetPriority, SetPriority method [BITS], SetPriority method [BITS],IBackgroundCopyJob interface, _drz_ibackgroundcopyjob_setpriority, bits.ibackgroundcopyjob_setpriority, bits/IBackgroundCopyJob::SetPriority
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
 - IBackgroundCopyJob::SetPriority
 - bits/IBackgroundCopyJob::SetPriority
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
 - IBackgroundCopyJob.SetPriority
---

# IBackgroundCopyJob::SetPriority


## -description

Specifies the priority level of your job. The priority level determines when your job is processed relative to other jobs in the transfer queue.

## -parameters

### -param Val [in]

Specifies the priority level of your job relative to other jobs in the transfer queue. The default is BG_JOB_PRIORITY_NORMAL. For a list of priority levels, see the 
<a href="/windows/desktop/api/bits/ne-bits-bg_job_priority">BG_JOB_PRIORITY</a> enumeration.

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
Job priority was successfully set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The value for <i>Priority</i> is not defined in the 
<a href="/windows/desktop/api/bits/ne-bits-bg_job_priority">BG_JOB_PRIORITY</a> enumeration.

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

## -see-also

<a href="/windows/desktop/api/bits/ne-bits-bg_job_priority">BG_JOB_PRIORITY</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-getpriority">IBackgroundCopyJob::GetPriority</a>