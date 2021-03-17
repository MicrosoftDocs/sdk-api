---
UID: NF:dskquota.IDiskQuotaControl.CreateUserBatch
title: IDiskQuotaControl::CreateUserBatch (dskquota.h)
description: Creates a batching object for optimizing updates to the quota settings of multiple users simultaneously.
helpviewer_keywords: ["CreateUserBatch","CreateUserBatch method [Files]","CreateUserBatch method [Files]","IDiskQuotaControl interface","IDiskQuotaControl interface [Files]","CreateUserBatch method","IDiskQuotaControl.CreateUserBatch","IDiskQuotaControl::CreateUserBatch","_win32_idiskquotacontrol_createuserbatch","base.idiskquotacontrol_createuserbatch","dskquota/IDiskQuotaControl::CreateUserBatch","fs.idiskquotacontrol_createuserbatch"]
old-location: fs\idiskquotacontrol_createuserbatch.htm
tech.root: fs
ms.assetid: c1c5a71f-4a2f-4bf9-b28f-11b87a558771
ms.date: 12/05/2018
ms.keywords: CreateUserBatch, CreateUserBatch method [Files], CreateUserBatch method [Files],IDiskQuotaControl interface, IDiskQuotaControl interface [Files],CreateUserBatch method, IDiskQuotaControl.CreateUserBatch, IDiskQuotaControl::CreateUserBatch, _win32_idiskquotacontrol_createuserbatch, base.idiskquotacontrol_createuserbatch, dskquota/IDiskQuotaControl::CreateUserBatch, fs.idiskquotacontrol_createuserbatch
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
 - IDiskQuotaControl::CreateUserBatch
 - dskquota/IDiskQuotaControl::CreateUserBatch
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
 - IDiskQuotaControl.CreateUserBatch
---

# IDiskQuotaControl::CreateUserBatch


## -description

Creates a batching object for optimizing updates to the quota settings of multiple users simultaneously.

## -parameters

### -param ppBatch [out]

A pointer to the 
<a href="/windows/desktop/api/dskquota/nn-dskquota-idiskquotauserbatch">IDiskQuotaUserBatch</a> interface pointer.

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
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller has insufficient access rights.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_READY</b></dt>
</dl>
</td>
<td width="60%">
The <b>DiskQuotaControl</b> object is not initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppBatch</i> parameter is <b>NULL</b>.

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



<a href="/windows/desktop/api/dskquota/nn-dskquota-idiskquotacontrol">IDiskQuotaControl</a>