---
UID: NF:qmgr.IBackgroundCopyGroup.CreateJob
title: IBackgroundCopyGroup::CreateJob (qmgr.h)
description: Use the CreateJob method to add a new job to the group. A group can contain only one job.
helpviewer_keywords: ["CreateJob","CreateJob method [BITS]","CreateJob method [BITS]","IBackgroundCopyGroup interface","IBackgroundCopyGroup interface [BITS]","CreateJob method","IBackgroundCopyGroup.CreateJob","IBackgroundCopyGroup::CreateJob","bits.ibackgroundcopygroup_createjob","qmgr/IBackgroundCopyGroup::CreateJob"]
old-location: bits\ibackgroundcopygroup_createjob.htm
tech.root: Bits
ms.assetid: 2453996e-f994-43b9-901b-680a55095268
ms.date: 12/05/2018
ms.keywords: CreateJob, CreateJob method [BITS], CreateJob method [BITS],IBackgroundCopyGroup interface, IBackgroundCopyGroup interface [BITS],CreateJob method, IBackgroundCopyGroup.CreateJob, IBackgroundCopyGroup::CreateJob, bits.ibackgroundcopygroup_createjob, qmgr/IBackgroundCopyGroup::CreateJob
req.header: qmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Qmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: QmgrPrxy.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyGroup::CreateJob
 - qmgr/IBackgroundCopyGroup::CreateJob
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
 - IBackgroundCopyGroup.CreateJob
---

# IBackgroundCopyGroup::CreateJob


## -description

<p class="CCE_Message">[<b>IBackgroundCopyGroup</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="/windows/desktop/Bits/bits-interfaces">BITS interfaces</a>.]

Use the <b>CreateJob</b> method to add a new job to the group. A group can contain only one job.

## -parameters

### -param guidJobID [in]

Uniquely identifies the job in the group and queue.

### -param ppJob [out]

Pointer to an <a href="/windows/desktop/api/qmgr/nn-qmgr-ibackgroundcopyjob1">IBackgroundCopyJob1</a> interface pointer. Use the interface to add files and check the state of the job.

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
The job was successfully created.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>QM_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The job is already running.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Only one job allowed per group.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/qmgr/nn-qmgr-ibackgroundcopygroup">IBackgroundCopyGroup</a>