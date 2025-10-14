---
UID: NF:qmgr.IBackgroundCopyGroup.CancelGroup
title: IBackgroundCopyGroup::CancelGroup (qmgr.h)
description: Use the CancelGroup method to remove the group from the queue. Files completely downloaded before calling this method are available to the client. You can cancel a group at anytime; however, the group cannot be recovered once it is canceled.
helpviewer_keywords: ["CancelGroup","CancelGroup method [BITS]","CancelGroup method [BITS]","IBackgroundCopyGroup interface","IBackgroundCopyGroup interface [BITS]","CancelGroup method","IBackgroundCopyGroup.CancelGroup","IBackgroundCopyGroup::CancelGroup","bits.ibackgroundcopygroup_cancelgroup","qmgr/IBackgroundCopyGroup::CancelGroup"]
old-location: bits\ibackgroundcopygroup_cancelgroup.htm
tech.root: Bits
ms.assetid: 4ef86db1-3dff-4345-a09a-efea8b6c8c8e
ms.date: 12/05/2018
ms.keywords: CancelGroup, CancelGroup method [BITS], CancelGroup method [BITS],IBackgroundCopyGroup interface, IBackgroundCopyGroup interface [BITS],CancelGroup method, IBackgroundCopyGroup.CancelGroup, IBackgroundCopyGroup::CancelGroup, bits.ibackgroundcopygroup_cancelgroup, qmgr/IBackgroundCopyGroup::CancelGroup
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
 - IBackgroundCopyGroup::CancelGroup
 - qmgr/IBackgroundCopyGroup::CancelGroup
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
 - IBackgroundCopyGroup.CancelGroup
---

# IBackgroundCopyGroup::CancelGroup


## -description

<p class="CCE_Message">[<b>IBackgroundCopyGroup</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="/windows/desktop/Bits/bits-interfaces">BITS interfaces</a>.]

Use the <b>CancelGroup</b> method to remove the group from the  queue. Files completely downloaded before calling this  method are available to the client. You can cancel a group at anytime; however, the group cannot be recovered once it is canceled.



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
The group was successfully canceled.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/qmgr/nn-qmgr-ibackgroundcopygroup">IBackgroundCopyGroup</a>
