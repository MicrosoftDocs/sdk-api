---
UID: NF:qmgr.IBackgroundCopyGroup.SuspendGroup
title: IBackgroundCopyGroup::SuspendGroup (qmgr.h)
description: Use the SuspendGroup method to pause a group in the download queue. New groups, groups that are in error, or groups that have finished downloading are automatically suspended.
helpviewer_keywords: ["IBackgroundCopyGroup interface [BITS]","SuspendGroup method","IBackgroundCopyGroup.SuspendGroup","IBackgroundCopyGroup::SuspendGroup","SuspendGroup","SuspendGroup method [BITS]","SuspendGroup method [BITS]","IBackgroundCopyGroup interface","bits.ibackgroundcopygroup_suspendgroup","qmgr/IBackgroundCopyGroup::SuspendGroup"]
old-location: bits\ibackgroundcopygroup_suspendgroup.htm
tech.root: Bits
ms.assetid: ac7600dd-3943-46cf-ad2d-f33d0099f2af
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyGroup interface [BITS],SuspendGroup method, IBackgroundCopyGroup.SuspendGroup, IBackgroundCopyGroup::SuspendGroup, SuspendGroup, SuspendGroup method [BITS], SuspendGroup method [BITS],IBackgroundCopyGroup interface, bits.ibackgroundcopygroup_suspendgroup, qmgr/IBackgroundCopyGroup::SuspendGroup
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
 - IBackgroundCopyGroup::SuspendGroup
 - qmgr/IBackgroundCopyGroup::SuspendGroup
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
 - IBackgroundCopyGroup.SuspendGroup
---

# IBackgroundCopyGroup::SuspendGroup


## -description

<p class="CCE_Message">[<b>IBackgroundCopyGroup</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="/windows/desktop/Bits/bits-interfaces">BITS interfaces</a>.]

Use the <b>SuspendGroup</b> method to pause a group in the download queue. New groups, groups that are in error, or groups that have finished downloading are automatically suspended.



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
Successfully suspended the group in the download queue.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/qmgr/nn-qmgr-ibackgroundcopygroup">IBackgroundCopyGroup</a>
