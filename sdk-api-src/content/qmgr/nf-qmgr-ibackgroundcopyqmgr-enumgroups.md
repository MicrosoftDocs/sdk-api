---
UID: NF:qmgr.IBackgroundCopyQMgr.EnumGroups
title: IBackgroundCopyQMgr::EnumGroups (qmgr.h)
description: Use the EnumGroups method to retrieve a list of groups that the current user owns. If the current user has Administrator privileges, the method returns all groups in the queue.
helpviewer_keywords: ["EnumGroups","EnumGroups method [BITS]","EnumGroups method [BITS]","IBackgroundCopyQMgr interface","IBackgroundCopyQMgr interface [BITS]","EnumGroups method","IBackgroundCopyQMgr.EnumGroups","IBackgroundCopyQMgr::EnumGroups","bits.ibackgroundcopyqmgr_enumgroups","qmgr/IBackgroundCopyQMgr::EnumGroups"]
old-location: bits\ibackgroundcopyqmgr_enumgroups.htm
tech.root: Bits
ms.assetid: 27cf17e3-b35a-4453-ae0a-8b080fd120dc
ms.date: 12/05/2018
ms.keywords: EnumGroups, EnumGroups method [BITS], EnumGroups method [BITS],IBackgroundCopyQMgr interface, IBackgroundCopyQMgr interface [BITS],EnumGroups method, IBackgroundCopyQMgr.EnumGroups, IBackgroundCopyQMgr::EnumGroups, bits.ibackgroundcopyqmgr_enumgroups, qmgr/IBackgroundCopyQMgr::EnumGroups
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
 - IBackgroundCopyQMgr::EnumGroups
 - qmgr/IBackgroundCopyQMgr::EnumGroups
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
 - IBackgroundCopyQMgr.EnumGroups
---

# IBackgroundCopyQMgr::EnumGroups


## -description

<p class="CCE_Message">[<b>IBackgroundCopyQMgr</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="/windows/desktop/Bits/bits-interfaces">BITS interfaces</a>.]

Use the <b>EnumGroups</b> method to retrieve a list of groups that the current user owns. If the current user has Administrator privileges, the method returns all groups in the queue.

## -parameters

### -param dwFlags [in]

Must be 0.

### -param ppEnumGroups [out]

Pointer to an <a href="/windows/desktop/api/qmgr/nn-qmgr-ienumbackgroundcopygroups">IEnumBackgroundCopyGroups</a> interface pointer. Use this interface to retrieve a group from the list.

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
Successfully retrieved a list of the groups in the download queue.

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

<a href="/windows/desktop/api/qmgr/nn-qmgr-ibackgroundcopyqmgr">IBackgroundCopyQMgr</a>