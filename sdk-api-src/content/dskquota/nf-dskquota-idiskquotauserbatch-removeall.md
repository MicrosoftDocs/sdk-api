---
UID: NF:dskquota.IDiskQuotaUserBatch.RemoveAll
title: IDiskQuotaUserBatch::RemoveAll (dskquota.h)
description: Removes all IDiskQuotaUser pointers from the batch list.
helpviewer_keywords: ["IDiskQuotaUserBatch interface [Files]","RemoveAll method","IDiskQuotaUserBatch.RemoveAll","IDiskQuotaUserBatch::RemoveAll","RemoveAll","RemoveAll method [Files]","RemoveAll method [Files]","IDiskQuotaUserBatch interface","_win32_idiskquotauserbatch_removeall","base.idiskquotauserbatch_removeall","dskquota/IDiskQuotaUserBatch::RemoveAll","fs.idiskquotauserbatch_removeall"]
old-location: fs\idiskquotauserbatch_removeall.htm
tech.root: fs
ms.assetid: f3c791a9-4976-4e04-903f-a1afffd01f7c
ms.date: 12/05/2018
ms.keywords: IDiskQuotaUserBatch interface [Files],RemoveAll method, IDiskQuotaUserBatch.RemoveAll, IDiskQuotaUserBatch::RemoveAll, RemoveAll, RemoveAll method [Files], RemoveAll method [Files],IDiskQuotaUserBatch interface, _win32_idiskquotauserbatch_removeall, base.idiskquotauserbatch_removeall, dskquota/IDiskQuotaUserBatch::RemoveAll, fs.idiskquotauserbatch_removeall
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
 - IDiskQuotaUserBatch::RemoveAll
 - dskquota/IDiskQuotaUserBatch::RemoveAll
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
 - IDiskQuotaUserBatch.RemoveAll
---

# IDiskQuotaUserBatch::RemoveAll


## -description

Removes all 
<a href="/windows/desktop/api/dskquota/nn-dskquota-idiskquotauser">IDiskQuotaUser</a> pointers from the batch list.



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
