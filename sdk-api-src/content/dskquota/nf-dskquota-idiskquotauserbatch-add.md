---
UID: NF:dskquota.IDiskQuotaUserBatch.Add
title: IDiskQuotaUserBatch::Add (dskquota.h)
description: Adds an IDiskQuotaUser pointer to the batch list.
helpviewer_keywords: ["Add","Add method [Files]","Add method [Files]","IDiskQuotaUserBatch interface","IDiskQuotaUserBatch interface [Files]","Add method","IDiskQuotaUserBatch.Add","IDiskQuotaUserBatch::Add","_win32_idiskquotauserbatch_add","base.idiskquotauserbatch_add","dskquota/IDiskQuotaUserBatch::Add","fs.idiskquotauserbatch_add"]
old-location: fs\idiskquotauserbatch_add.htm
tech.root: fs
ms.assetid: 8b0876d2-55ba-4eaa-b317-8ea1d2f5ff4f
ms.date: 12/05/2018
ms.keywords: Add, Add method [Files], Add method [Files],IDiskQuotaUserBatch interface, IDiskQuotaUserBatch interface [Files],Add method, IDiskQuotaUserBatch.Add, IDiskQuotaUserBatch::Add, _win32_idiskquotauserbatch_add, base.idiskquotauserbatch_add, dskquota/IDiskQuotaUserBatch::Add, fs.idiskquotauserbatch_add
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
 - IDiskQuotaUserBatch::Add
 - dskquota/IDiskQuotaUserBatch::Add
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
 - IDiskQuotaUserBatch.Add
---

# IDiskQuotaUserBatch::Add


## -description

Adds an 
<a href="/windows/desktop/api/dskquota/nn-dskquota-idiskquotauser">IDiskQuotaUser</a> pointer to the batch list. This method calls <b>AddRef</b> on the <i>pUser</i> interface pointer. <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> is automatically called on each contained 
<a href="/windows/desktop/api/dskquota/nn-dskquota-idiskquotauser">IDiskQuotaUser</a> interface pointer when the batch object is destroyed.

When setting values on a quota user object in preparation for batch processing, specify <b>FALSE</b> for the <i>fWriteThrough</i> parameter in the 
<a href="/windows/desktop/api/dskquota/nf-dskquota-idiskquotauser-setquotalimit">IDiskQuotaUser::SetQuotaLimit</a> and 
<a href="/windows/desktop/api/dskquota/nf-dskquota-idiskquotauser-setquotathreshold">IDiskQuotaUser::SetQuotaThreshold</a> methods. This stores the values in memory without writing to disk. To write the changes to disk, call the 
<a href="/windows/desktop/api/dskquota/nf-dskquota-idiskquotauserbatch-flushtodisk">IDiskQuotaUserBatch::FlushToDisk</a> method.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

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