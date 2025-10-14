---
UID: NF:bits.IBackgroundCopyJob.GetState
title: IBackgroundCopyJob::GetState (bits.h)
description: Retrieves the state of the job.
helpviewer_keywords: ["GetState","GetState method [BITS]","GetState method [BITS]","IBackgroundCopyJob interface","IBackgroundCopyJob interface [BITS]","GetState method","IBackgroundCopyJob.GetState","IBackgroundCopyJob::GetState","_drz_ibackgroundcopyjob_getstate","bits.ibackgroundcopyjob_getstate","bits/IBackgroundCopyJob::GetState"]
old-location: bits\ibackgroundcopyjob_getstate.htm
tech.root: Bits
ms.assetid: 32789bd2-2368-473b-accf-ac6e317d0172
ms.date: 12/05/2018
ms.keywords: GetState, GetState method [BITS], GetState method [BITS],IBackgroundCopyJob interface, IBackgroundCopyJob interface [BITS],GetState method, IBackgroundCopyJob.GetState, IBackgroundCopyJob::GetState, _drz_ibackgroundcopyjob_getstate, bits.ibackgroundcopyjob_getstate, bits/IBackgroundCopyJob::GetState
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
 - IBackgroundCopyJob::GetState
 - bits/IBackgroundCopyJob::GetState
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
 - IBackgroundCopyJob.GetState
---

# IBackgroundCopyJob::GetState


## -description

Retrieves the state of the job.

## -parameters

### -param pVal [out]

The state of the job. For example, the state reflects whether the job is in error, transferring data, or suspended. For a list of job states, see the 
<a href="/windows/desktop/api/bits/ne-bits-bg_job_state">BG_JOB_STATE</a> enumeration.

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
The state of the job was successfully retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The parameter, <i>pJobState</i>, cannot be <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

If you want to know when a job is in error or has transferred all the files in the job, you can use this method to poll for the state of the job or you can register to receive notification when  events occur. For details on registering to receive event notification, see the 
<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopycallback">IBackgroundCopyCallback</a> interface.

## Examples

See the example code for the [IBackgroundCopyManager::GetJob](./nf-bits-ibackgroundcopymanager-getjob.md) method.

## -see-also

[BG_JOB_STATE](/windows/desktop/api/bits/ne-bits-bg_job_state), [Determining the status of a job](/windows/desktop/Bits/determining-the-status-of-a-job), [IBackgroundCopyCallback](/windows/desktop/api/bits/nn-bits-ibackgroundcopycallback)