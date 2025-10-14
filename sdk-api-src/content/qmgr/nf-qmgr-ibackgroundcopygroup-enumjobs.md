---
UID: NF:qmgr.IBackgroundCopyGroup.EnumJobs
title: IBackgroundCopyGroup::EnumJobs (qmgr.h)
description: Use the EnumJobs method to retrieve a list of jobs in the group. The list contains only one job.
helpviewer_keywords: ["EnumJobs","EnumJobs method [BITS]","EnumJobs method [BITS]","IBackgroundCopyGroup interface","IBackgroundCopyGroup interface [BITS]","EnumJobs method","IBackgroundCopyGroup.EnumJobs","IBackgroundCopyGroup::EnumJobs","bits.ibackgroundcopygroup_enumjobs","qmgr/IBackgroundCopyGroup::EnumJobs"]
old-location: bits\ibackgroundcopygroup_enumjobs.htm
tech.root: Bits
ms.assetid: 40e4412e-60d5-4e08-85b9-1e92f5222e71
ms.date: 12/05/2018
ms.keywords: EnumJobs, EnumJobs method [BITS], EnumJobs method [BITS],IBackgroundCopyGroup interface, IBackgroundCopyGroup interface [BITS],EnumJobs method, IBackgroundCopyGroup.EnumJobs, IBackgroundCopyGroup::EnumJobs, bits.ibackgroundcopygroup_enumjobs, qmgr/IBackgroundCopyGroup::EnumJobs
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
 - IBackgroundCopyGroup::EnumJobs
 - qmgr/IBackgroundCopyGroup::EnumJobs
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
 - IBackgroundCopyGroup.EnumJobs
---

# IBackgroundCopyGroup::EnumJobs


## -description

<p class="CCE_Message">[<b>IBackgroundCopyGroup</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="/windows/desktop/Bits/bits-interfaces">BITS interfaces</a>.]

Use the <b>EnumJobs</b> method to retrieve a list of jobs in the group. The list contains only one job.

## -parameters

### -param dwFlags [in]

Must be 0.

### -param ppEnumJobs [out]

Pointer to an <a href="/windows/desktop/api/qmgr/nn-qmgr-ienumbackgroundcopyjobs1">IEnumBackgroundCopyJobs1</a> interface pointer. Use the interface to iterate through the list of jobs.

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
Successfully enumerated the jobs in the group.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwFlags</i> parameter must be 0.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/qmgr/nn-qmgr-ibackgroundcopygroup">IBackgroundCopyGroup</a>