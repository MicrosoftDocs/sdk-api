---
UID: NF:qmgr.IBackgroundCopyQMgr.GetGroup
title: IBackgroundCopyQMgr::GetGroup (qmgr.h)
description: Use the GetGroup method to retrieve a group from the download queue.
helpviewer_keywords: ["GetGroup","GetGroup method [BITS]","GetGroup method [BITS]","IBackgroundCopyQMgr interface","IBackgroundCopyQMgr interface [BITS]","GetGroup method","IBackgroundCopyQMgr.GetGroup","IBackgroundCopyQMgr::GetGroup","bits.ibackgroundcopyqmgr_getgroup","qmgr/IBackgroundCopyQMgr::GetGroup"]
old-location: bits\ibackgroundcopyqmgr_getgroup.htm
tech.root: Bits
ms.assetid: 36836fe5-4858-4c6e-8ce8-1bb71c8e9f5a
ms.date: 12/05/2018
ms.keywords: GetGroup, GetGroup method [BITS], GetGroup method [BITS],IBackgroundCopyQMgr interface, IBackgroundCopyQMgr interface [BITS],GetGroup method, IBackgroundCopyQMgr.GetGroup, IBackgroundCopyQMgr::GetGroup, bits.ibackgroundcopyqmgr_getgroup, qmgr/IBackgroundCopyQMgr::GetGroup
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
 - IBackgroundCopyQMgr::GetGroup
 - qmgr/IBackgroundCopyQMgr::GetGroup
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
 - IBackgroundCopyQMgr.GetGroup
---

# IBackgroundCopyQMgr::GetGroup


## -description

<p class="CCE_Message">[<a href="/windows/desktop/api/qmgr/nn-qmgr-ibackgroundcopyqmgr">IBackgroundCopyQMgr</a> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="/windows/desktop/Bits/bits-interfaces">BITS interfaces</a>.]

Use the <b>GetGroup</b> method to retrieve a group from the download queue. The current user can retrieve only groups that they own. If the user has Administrator privileges, the user can retrieve any group from the download queue. Retrieving a group from the queue transfers ownership of the group to the current user.

## -parameters

### -param groupID [in]

GUID that uniquely identifies the group in the download queue.

### -param ppGroup [out]

Pointer to an <a href="/windows/desktop/api/qmgr/nn-qmgr-ibackgroundcopygroup">IBackgroundCopyGroup</a> interface pointer. Use this interface to manage the group. For example, add a job to the group and set the properties of the group.

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
Successfully retrieved the group. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>QM_E_ITEM_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Could not find the group in the download queue.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/qmgr/nn-qmgr-ibackgroundcopyqmgr">IBackgroundCopyQMgr</a>