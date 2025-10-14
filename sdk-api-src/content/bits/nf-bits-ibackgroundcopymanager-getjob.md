---
UID: NF:bits.IBackgroundCopyManager.GetJob
title: IBackgroundCopyManager::GetJob (bits.h)
description: Retrieves a specified job from the transfer queue. Typically, your application persists the job identifier, so you can later retrieve the job from the queue.
helpviewer_keywords: ["GetJob","GetJob method [BITS]","GetJob method [BITS]","IBackgroundCopyManager interface","IBackgroundCopyManager interface [BITS]","GetJob method","IBackgroundCopyManager.GetJob","IBackgroundCopyManager::GetJob","_drz_ibackgroundcopymanager_getjob","bits.ibackgroundcopymanager_getjob","bits/IBackgroundCopyManager::GetJob"]
old-location: bits\ibackgroundcopymanager_getjob.htm
tech.root: Bits
ms.assetid: dbb7cae6-7e9c-4ac5-8f02-372acaa4fb4d
ms.date: 12/05/2018
ms.keywords: GetJob, GetJob method [BITS], GetJob method [BITS],IBackgroundCopyManager interface, IBackgroundCopyManager interface [BITS],GetJob method, IBackgroundCopyManager.GetJob, IBackgroundCopyManager::GetJob, _drz_ibackgroundcopymanager_getjob, bits.ibackgroundcopymanager_getjob, bits/IBackgroundCopyManager::GetJob
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
 - IBackgroundCopyManager::GetJob
 - bits/IBackgroundCopyManager::GetJob
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
 - IBackgroundCopyManager.GetJob
---

# IBackgroundCopyManager::GetJob


## -description

Retrieves a specified job from the transfer queue. Typically, your application persists the job identifier, so you can later retrieve the job from the queue.

## -parameters

### -param jobID [in]

Identifies the job to retrieve from the transfer queue. The 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopymanager-createjob">CreateJob</a> method returns the job identifier.

### -param ppJob [out]

An 
<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyjob">IBackgroundCopyJob</a> interface pointer to the job specified by <i>JobID</i>. When done, release <i>ppJob</i>.

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
Job was successfully retrieved from the transfer queue.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The job was not found in the queue.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
User does not have permission to retrieve the job.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyjob">IBackgroundCopyJob</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-getid">IBackgroundCopyJob::GetId</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopymanager-createjob">IBackgroundCopyManager::CreateJob</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopymanager-enumjobs">IBackgroundCopyManager::EnumJobs</a>