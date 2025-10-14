---
UID: NF:qmgr.IBackgroundCopyGroup.GetJob
title: IBackgroundCopyGroup::GetJob (qmgr.h)
description: Use the GetJob method to retrieve a job from the group.
helpviewer_keywords: ["GetJob","GetJob method [BITS]","GetJob method [BITS]","IBackgroundCopyGroup interface","IBackgroundCopyGroup interface [BITS]","GetJob method","IBackgroundCopyGroup.GetJob","IBackgroundCopyGroup::GetJob","bits.ibackgroundcopygroup_getjob","qmgr/IBackgroundCopyGroup::GetJob"]
old-location: bits\ibackgroundcopygroup_getjob.htm
tech.root: Bits
ms.assetid: c392e9e2-0489-457b-b21a-dfff9e2c0f39
ms.date: 12/05/2018
ms.keywords: GetJob, GetJob method [BITS], GetJob method [BITS],IBackgroundCopyGroup interface, IBackgroundCopyGroup interface [BITS],GetJob method, IBackgroundCopyGroup.GetJob, IBackgroundCopyGroup::GetJob, bits.ibackgroundcopygroup_getjob, qmgr/IBackgroundCopyGroup::GetJob
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
 - IBackgroundCopyGroup::GetJob
 - qmgr/IBackgroundCopyGroup::GetJob
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
 - IBackgroundCopyGroup.GetJob
---

# IBackgroundCopyGroup::GetJob


## -description

<p class="CCE_Message">[<b>IBackgroundCopyGroup</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="/windows/desktop/Bits/bits-interfaces">BITS interfaces</a>.]

Use the <b>GetJob</b> method to retrieve a job from the group.

## -parameters

### -param jobID [in]

Identifies the job to retrieve.

### -param ppJob [out]

Pointer to an <a href="/windows/desktop/api/qmgr/nn-qmgr-ibackgroundcopyjob1">IBackgroundCopyJob1</a> interface pointer. Use the interface to add files and retrieve the state of the job.

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
Successfully retrieved the job from the group.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>QM_E_ITEM_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Could not find the job in the group.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/qmgr/nn-qmgr-ibackgroundcopygroup">IBackgroundCopyGroup</a>