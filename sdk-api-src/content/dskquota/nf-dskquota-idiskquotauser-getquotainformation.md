---
UID: NF:dskquota.IDiskQuotaUser.GetQuotaInformation
title: IDiskQuotaUser::GetQuotaInformation (dskquota.h)
description: Retrieves the values for the user's warning threshold, hard quota limit, and quota used.
helpviewer_keywords: ["GetQuotaInformation","GetQuotaInformation method [Files]","GetQuotaInformation method [Files]","IDiskQuotaUser interface","IDiskQuotaUser interface [Files]","GetQuotaInformation method","IDiskQuotaUser.GetQuotaInformation","IDiskQuotaUser::GetQuotaInformation","_win32_idiskquotauser_getquotainformation","base.idiskquotauser_getquotainformation","dskquota/IDiskQuotaUser::GetQuotaInformation","fs.idiskquotauser_getquotainformation"]
old-location: fs\idiskquotauser_getquotainformation.htm
tech.root: fs
ms.assetid: d1640803-965a-473c-bf10-bee51d47fcfa
ms.date: 12/05/2018
ms.keywords: GetQuotaInformation, GetQuotaInformation method [Files], GetQuotaInformation method [Files],IDiskQuotaUser interface, IDiskQuotaUser interface [Files],GetQuotaInformation method, IDiskQuotaUser.GetQuotaInformation, IDiskQuotaUser::GetQuotaInformation, _win32_idiskquotauser_getquotainformation, base.idiskquotauser_getquotainformation, dskquota/IDiskQuotaUser::GetQuotaInformation, fs.idiskquotauser_getquotainformation
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
 - IDiskQuotaUser::GetQuotaInformation
 - dskquota/IDiskQuotaUser::GetQuotaInformation
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
 - IDiskQuotaUser.GetQuotaInformation
---

# IDiskQuotaUser::GetQuotaInformation


## -description

Retrieves the values for the user's warning threshold, hard quota limit, and quota used.

## -parameters

### -param pbQuotaInfo [out]

A pointer to the 
[DISKQUOTA_USER_INFORMATION](./ns-dskquota-diskquota_user_information.md) structure to receive the quota information.

### -param cbQuotaInfo [in]

The size of the quota information structure, in bytes.

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
<dt><b>ERROR_LOCK_FAILED</b></dt>
</dl>
</td>
<td width="60%">
Failure to obtain an exclusive lock.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pQuotaInfo</i> parameter is <b>NULL</b>.

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

## -see-also

<a href="/windows/desktop/FileIO/disk-management-interfaces">Disk Management Interfaces</a>



<a href="/windows/desktop/FileIO/managing-disk-quotas">Disk Quotas</a>



<a href="/windows/desktop/api/dskquota/nn-dskquota-idiskquotauser">IDiskQuotaUser</a>