---
UID: NF:bits.IBackgroundCopyJob.Suspend
title: IBackgroundCopyJob::Suspend (bits.h)
description: Suspends a job. New jobs, jobs that are in error, and jobs that have finished transferring files are automatically suspended.
helpviewer_keywords: ["IBackgroundCopyJob interface [BITS]","Suspend method","IBackgroundCopyJob.Suspend","IBackgroundCopyJob::Suspend","Suspend","Suspend method [BITS]","Suspend method [BITS]","IBackgroundCopyJob interface","_drz_ibackgroundcopyjob_suspend","bits.ibackgroundcopyjob_suspend","bits/IBackgroundCopyJob::Suspend"]
old-location: bits\ibackgroundcopyjob_suspend.htm
tech.root: Bits
ms.assetid: 88429730-b8e5-4969-934c-f0945fdd46a6
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyJob interface [BITS],Suspend method, IBackgroundCopyJob.Suspend, IBackgroundCopyJob::Suspend, Suspend, Suspend method [BITS], Suspend method [BITS],IBackgroundCopyJob interface, _drz_ibackgroundcopyjob_suspend, bits.ibackgroundcopyjob_suspend, bits/IBackgroundCopyJob::Suspend
f1_keywords:
- bits/IBackgroundCopyJob.Suspend
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- QmgrPrxy.dll
api_name:
- IBackgroundCopyJob.Suspend
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBackgroundCopyJob::Suspend


## -description


Suspends a job. New jobs, jobs that are in error, and jobs that have finished transferring files are automatically suspended.


## -parameters






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
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
Successfully suspended the job.

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




<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-cancel">IBackgroundCopyJob::Cancel</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-resume">IBackgroundCopyJob::Resume</a>
 

 

