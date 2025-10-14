---
UID: NF:qmgr.IBackgroundCopyQMgr.CreateGroup
title: IBackgroundCopyQMgr::CreateGroup (qmgr.h)
description: Use the CreateGroup method to create a new group and add it to the download queue.
helpviewer_keywords: ["CreateGroup","CreateGroup method [BITS]","CreateGroup method [BITS]","IBackgroundCopyQMgr interface","IBackgroundCopyQMgr interface [BITS]","CreateGroup method","IBackgroundCopyQMgr.CreateGroup","IBackgroundCopyQMgr::CreateGroup","bits.ibackgroundcopyqmgr_creategroup","qmgr/IBackgroundCopyQMgr::CreateGroup"]
old-location: bits\ibackgroundcopyqmgr_creategroup.htm
tech.root: Bits
ms.assetid: d64fec33-3781-428e-af9d-4a08836760d2
ms.date: 12/05/2018
ms.keywords: CreateGroup, CreateGroup method [BITS], CreateGroup method [BITS],IBackgroundCopyQMgr interface, IBackgroundCopyQMgr interface [BITS],CreateGroup method, IBackgroundCopyQMgr.CreateGroup, IBackgroundCopyQMgr::CreateGroup, bits.ibackgroundcopyqmgr_creategroup, qmgr/IBackgroundCopyQMgr::CreateGroup
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
 - IBackgroundCopyQMgr::CreateGroup
 - qmgr/IBackgroundCopyQMgr::CreateGroup
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
 - IBackgroundCopyQMgr.CreateGroup
---

# IBackgroundCopyQMgr::CreateGroup


## -description

<p class="CCE_Message">[<b>IBackgroundCopyQMgr</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="/windows/desktop/Bits/bits-interfaces">BITS interfaces</a>.]

Use the <b>CreateGroup</b> method to create a new group and add it to the download queue.

## -parameters

### -param guidGroupID [in]

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
Successfully created the group.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
A group already exists with that GUID.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/qmgr/nn-qmgr-ibackgroundcopyqmgr">IBackgroundCopyQMgr</a>