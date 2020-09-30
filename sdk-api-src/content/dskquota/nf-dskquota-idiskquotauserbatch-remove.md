---
UID: NF:dskquota.IDiskQuotaUserBatch.Remove
title: IDiskQuotaUserBatch::Remove (dskquota.h)
description: Removes an IDiskQuotaUser pointer from the batch list.
helpviewer_keywords: ["IDiskQuotaUserBatch interface [Files]","Remove method","IDiskQuotaUserBatch.Remove","IDiskQuotaUserBatch::Remove","Remove","Remove method [Files]","Remove method [Files]","IDiskQuotaUserBatch interface","_win32_idiskquotauserbatch_remove","base.idiskquotauserbatch_remove","dskquota/IDiskQuotaUserBatch::Remove","fs.idiskquotauserbatch_remove"]
old-location: fs\idiskquotauserbatch_remove.htm
tech.root: fs
ms.assetid: 102e9a07-9958-4d47-acd3-6b81e83a5ea7
ms.date: 12/05/2018
ms.keywords: IDiskQuotaUserBatch interface [Files],Remove method, IDiskQuotaUserBatch.Remove, IDiskQuotaUserBatch::Remove, Remove, Remove method [Files], Remove method [Files],IDiskQuotaUserBatch interface, _win32_idiskquotauserbatch_remove, base.idiskquotauserbatch_remove, dskquota/IDiskQuotaUserBatch::Remove, fs.idiskquotauserbatch_remove
req.header: dskquota.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Dskquota.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDiskQuotaUserBatch::Remove
 - dskquota/IDiskQuotaUserBatch::Remove
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dskquota.dll
api_name:
 - IDiskQuotaUserBatch.Remove
---

# IDiskQuotaUserBatch::Remove


## -description

Removes an 
<a href="/windows/desktop/api/dskquota/nn-dskquota-idiskquotauser">IDiskQuotaUser</a> pointer from the batch list.

## -parameters

### -param pUser [in]

A pointer to the quota user object's 
<a href="/windows/desktop/api/dskquota/nn-dskquota-idiskquotauser">IDiskQuotaUser</a> interface.

## -returns

This method returns one of the following values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Quota user object not found in batch.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pUser</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected exception occurred.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/FileIO/disk-management-interfaces">Disk Management Interfaces</a>



<a href="/windows/desktop/FileIO/managing-disk-quotas">Disk Quotas</a>



<a href="/windows/desktop/api/dskquota/nn-dskquota-idiskquotauserbatch">IDiskQuotaUserBatch</a>