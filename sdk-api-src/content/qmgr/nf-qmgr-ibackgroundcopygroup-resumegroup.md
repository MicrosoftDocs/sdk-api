---
UID: NF:qmgr.IBackgroundCopyGroup.ResumeGroup
title: IBackgroundCopyGroup::ResumeGroup (qmgr.h)
description: Use the ResumeGroup method to start a group that has been suspended in the download queue.
helpviewer_keywords: ["IBackgroundCopyGroup interface [BITS]","ResumeGroup method","IBackgroundCopyGroup.ResumeGroup","IBackgroundCopyGroup::ResumeGroup","ResumeGroup","ResumeGroup method [BITS]","ResumeGroup method [BITS]","IBackgroundCopyGroup interface","bits.ibackgroundcopygroup_resumegroup","qmgr/IBackgroundCopyGroup::ResumeGroup"]
old-location: bits\ibackgroundcopygroup_resumegroup.htm
tech.root: Bits
ms.assetid: a9b0b7df-9149-4d09-a37c-c0a4f5dc6e45
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyGroup interface [BITS],ResumeGroup method, IBackgroundCopyGroup.ResumeGroup, IBackgroundCopyGroup::ResumeGroup, ResumeGroup, ResumeGroup method [BITS], ResumeGroup method [BITS],IBackgroundCopyGroup interface, bits.ibackgroundcopygroup_resumegroup, qmgr/IBackgroundCopyGroup::ResumeGroup
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
 - IBackgroundCopyGroup::ResumeGroup
 - qmgr/IBackgroundCopyGroup::ResumeGroup
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
 - IBackgroundCopyGroup.ResumeGroup
---

# IBackgroundCopyGroup::ResumeGroup


## -description

<p class="CCE_Message">[<b>IBackgroundCopyGroup</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="/windows/desktop/Bits/bits-interfaces">BITS interfaces</a>.]

Use the <b>ResumeGroup</b> method to start a group that has been suspended in the download queue.



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
Successfully resumed the group in the download queue.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/qmgr/nn-qmgr-ibackgroundcopygroup">IBackgroundCopyGroup</a>
