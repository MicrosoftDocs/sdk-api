---
UID: NF:bits.IBackgroundCopyJob.GetType
title: IBackgroundCopyJob::GetType (bits.h)
description: Retrieves the type of transfer being performed, such as a file download or upload.
helpviewer_keywords: ["GetType","GetType method [BITS]","GetType method [BITS]","IBackgroundCopyJob interface","IBackgroundCopyJob interface [BITS]","GetType method","IBackgroundCopyJob.GetType","IBackgroundCopyJob::GetType","_drz_ibackgroundcopyjob_gettype","bits.ibackgroundcopyjob_gettype","bits/IBackgroundCopyJob::GetType"]
old-location: bits\ibackgroundcopyjob_gettype.htm
tech.root: Bits
ms.assetid: b84c45c2-379a-40d0-91ab-0124f0ef6b00
ms.date: 12/05/2018
ms.keywords: GetType, GetType method [BITS], GetType method [BITS],IBackgroundCopyJob interface, IBackgroundCopyJob interface [BITS],GetType method, IBackgroundCopyJob.GetType, IBackgroundCopyJob::GetType, _drz_ibackgroundcopyjob_gettype, bits.ibackgroundcopyjob_gettype, bits/IBackgroundCopyJob::GetType
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
 - IBackgroundCopyJob::GetType
 - bits/IBackgroundCopyJob::GetType
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
 - IBackgroundCopyJob.GetType
---

# IBackgroundCopyJob::GetType


## -description

Retrieves the type of transfer being performed, such as a file download or upload.

## -parameters

### -param pVal [out]

Type of transfer being performed. For a list of transfer types, see the 
<a href="/windows/desktop/api/bits/ne-bits-bg_job_type">BG_JOB_TYPE</a> enumeration.

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
Transfer type was successfully retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pJobType</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

Specify the type of transfer when you 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopymanager-createjob">create the job</a>.

## -see-also

<a href="/windows/desktop/api/bits/ne-bits-bg_job_type">BG_JOB_TYPE</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopymanager-createjob">IBackgroundCopyManager::CreateJob</a>