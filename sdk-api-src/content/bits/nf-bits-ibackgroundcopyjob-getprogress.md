---
UID: NF:bits.IBackgroundCopyJob.GetProgress
title: IBackgroundCopyJob::GetProgress (bits.h)
description: Retrieves job-related progress information, such as the number of bytes and files transferred.
helpviewer_keywords: ["GetProgress","GetProgress method [BITS]","GetProgress method [BITS]","IBackgroundCopyJob interface","IBackgroundCopyJob interface [BITS]","GetProgress method","IBackgroundCopyJob.GetProgress","IBackgroundCopyJob::GetProgress","_drz_ibackgroundcopyjob_getprogress","bits.ibackgroundcopyjob_getprogress","bits/IBackgroundCopyJob::GetProgress"]
old-location: bits\ibackgroundcopyjob_getprogress.htm
tech.root: Bits
ms.assetid: 30aae990-1cc1-468b-9e5f-7ef5ce6eeb9a
ms.date: 12/05/2018
ms.keywords: GetProgress, GetProgress method [BITS], GetProgress method [BITS],IBackgroundCopyJob interface, IBackgroundCopyJob interface [BITS],GetProgress method, IBackgroundCopyJob.GetProgress, IBackgroundCopyJob::GetProgress, _drz_ibackgroundcopyjob_getprogress, bits.ibackgroundcopyjob_getprogress, bits/IBackgroundCopyJob::GetProgress
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
 - IBackgroundCopyJob::GetProgress
 - bits/IBackgroundCopyJob::GetProgress
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
 - IBackgroundCopyJob.GetProgress
---

# IBackgroundCopyJob::GetProgress


## -description

Retrieves job-related progress information, such as the number of bytes and files transferred.

## -parameters

### -param pVal [out]

Contains data that you can use to calculate the percentage of the job that is complete. For more information, see 
<a href="/windows/desktop/api/bits/ns-bits-bg_job_progress">BG_JOB_PROGRESS</a>.

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
Progress information was successfully retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pProgress</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/bits/ns-bits-bg_job_progress">BG_JOB_PROGRESS</a>