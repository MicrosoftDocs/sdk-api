---
UID: NF:dskquota.IDiskQuotaUserBatch.FlushToDisk
title: IDiskQuotaUserBatch::FlushToDisk (dskquota.h)
description: Writes user object changes to disk in a single call to the underlying file system.
helpviewer_keywords: ["FlushToDisk","FlushToDisk method [Files]","FlushToDisk method [Files]","IDiskQuotaUserBatch interface","IDiskQuotaUserBatch interface [Files]","FlushToDisk method","IDiskQuotaUserBatch.FlushToDisk","IDiskQuotaUserBatch::FlushToDisk","_win32_idiskquotauserbatch_flushtodisk","base.idiskquotauserbatch_flushtodisk","dskquota/IDiskQuotaUserBatch::FlushToDisk","fs.idiskquotauserbatch_flushtodisk"]
old-location: fs\idiskquotauserbatch_flushtodisk.htm
tech.root: fs
ms.assetid: 2d147224-64d8-4c15-b860-e6dd216cb170
ms.date: 12/05/2018
ms.keywords: FlushToDisk, FlushToDisk method [Files], FlushToDisk method [Files],IDiskQuotaUserBatch interface, IDiskQuotaUserBatch interface [Files],FlushToDisk method, IDiskQuotaUserBatch.FlushToDisk, IDiskQuotaUserBatch::FlushToDisk, _win32_idiskquotauserbatch_flushtodisk, base.idiskquotauserbatch_flushtodisk, dskquota/IDiskQuotaUserBatch::FlushToDisk, fs.idiskquotauserbatch_flushtodisk
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
 - IDiskQuotaUserBatch::FlushToDisk
 - dskquota/IDiskQuotaUserBatch::FlushToDisk
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
 - IDiskQuotaUserBatch.FlushToDisk
---

# IDiskQuotaUserBatch::FlushToDisk


## -description

Writes user object changes to disk in a single call to the underlying file system.



## -returns

This method returns a file system error or one of the following values.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unexpected file system error occurred.

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

## -remarks

There are limitations on the amount of information that can be written to disk in a single call to the file system. The flush operation may generate multiple calls to the file system. Nonetheless, the batch operation will be more efficient than a single call for each user object.

## -see-also

<a href="/windows/desktop/FileIO/disk-management-interfaces">Disk Management Interfaces</a>



<a href="/windows/desktop/FileIO/managing-disk-quotas">Disk Quotas</a>



<a href="/windows/desktop/api/dskquota/nn-dskquota-idiskquotauserbatch">IDiskQuotaUserBatch</a>
