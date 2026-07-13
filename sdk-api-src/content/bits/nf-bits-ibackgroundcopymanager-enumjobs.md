---
UID: NF:bits.IBackgroundCopyManager.EnumJobs
title: IBackgroundCopyManager::EnumJobs (bits.h)
description: Retrieves an interface pointer to an enumerator object that you use to enumerate the jobs in the transfer queue. The order of the jobs in the enumerator is arbitrary.
helpviewer_keywords: ["BG_JOB_ENUM_ALL_USERS","EnumJobs","EnumJobs method [BITS]","EnumJobs method [BITS]","IBackgroundCopyManager interface","IBackgroundCopyManager interface [BITS]","EnumJobs method","IBackgroundCopyManager.EnumJobs","IBackgroundCopyManager::EnumJobs","_drz_ibackgroundcopymanager_enumjobs","bits.ibackgroundcopymanager_enumjobs","bits/IBackgroundCopyManager::EnumJobs"]
old-location: bits\ibackgroundcopymanager_enumjobs.htm
tech.root: Bits
ms.assetid: e8b73060-dff9-4ab3-8009-d2b41502fc1a
ms.date: 12/05/2018
ms.keywords: BG_JOB_ENUM_ALL_USERS, EnumJobs, EnumJobs method [BITS], EnumJobs method [BITS],IBackgroundCopyManager interface, IBackgroundCopyManager interface [BITS],EnumJobs method, IBackgroundCopyManager.EnumJobs, IBackgroundCopyManager::EnumJobs, _drz_ibackgroundcopymanager_enumjobs, bits.ibackgroundcopymanager_enumjobs, bits/IBackgroundCopyManager::EnumJobs
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
 - IBackgroundCopyManager::EnumJobs
 - bits/IBackgroundCopyManager::EnumJobs
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
 - IBackgroundCopyManager.EnumJobs
---

# IBackgroundCopyManager::EnumJobs


## -description

Retrieves an interface pointer to an enumerator object that you use to 
<a href="/windows/desktop/Bits/enumerating-jobs-in-the-transfer-queue">enumerate the jobs</a> in the transfer queue. The order of the jobs in the enumerator is arbitrary.

## -parameters

### -param dwFlags [in]

Specifies whose jobs to include in the enumeration. If <i>dwFlags</i> is set to 0, the user receives all jobs that they own in the transfer queue. The following table lists the enumeration options. 



<table>
<tr>
<th>Option</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BG_JOB_ENUM_ALL_USERS"></a><a id="bg_job_enum_all_users"></a><dl>
<dt><b>BG_JOB_ENUM_ALL_USERS</b></dt>
</dl>
</td>
<td width="60%">
Includes all jobs in the transfer queue—those owned by the user and those owned by others. The user must be an administrator to use this flag.

</td>
</tr>
</table>

### -param ppEnum [out]

An 
<a href="/windows/desktop/api/bits/nn-bits-ienumbackgroundcopyjobs">IEnumBackgroundCopyJobs</a> interface pointer that you use to enumerate the jobs in the transfer queue. The contents of the enumerator depend on the value of <i>dwFlags</i>. Release <i>ppEnumJobs</i> when done.

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
Successfully generated enumerator object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The user must be an administrator or belong to an administrator group to enumerate jobs owned by another user.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-enumfiles">IBackgroundCopyJob::EnumFiles</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopymanager-getjob">IBackgroundCopyManager::GetJob</a>



<a href="/windows/desktop/api/bits/nn-bits-ienumbackgroundcopyjobs">IEnumBackgroundCopyJobs</a>