---
UID: NF:dskquota.IDiskQuotaUser.SetQuotaThreshold
title: IDiskQuotaUser::SetQuotaThreshold (dskquota.h)
description: Sets the user's warning threshold value on the volume.
helpviewer_keywords: ["IDiskQuotaUser interface [Files]","SetQuotaThreshold method","IDiskQuotaUser.SetQuotaThreshold","IDiskQuotaUser::SetQuotaThreshold","SetQuotaThreshold","SetQuotaThreshold method [Files]","SetQuotaThreshold method [Files]","IDiskQuotaUser interface","_win32_idiskquotauser_setquotathreshold","base.idiskquotauser_setquotathreshold","dskquota/IDiskQuotaUser::SetQuotaThreshold","fs.idiskquotauser_setquotathreshold"]
old-location: fs\idiskquotauser_setquotathreshold.htm
tech.root: fs
ms.assetid: 7c641a1c-fb04-4039-92bd-d3a1c7045355
ms.date: 12/05/2018
ms.keywords: IDiskQuotaUser interface [Files],SetQuotaThreshold method, IDiskQuotaUser.SetQuotaThreshold, IDiskQuotaUser::SetQuotaThreshold, SetQuotaThreshold, SetQuotaThreshold method [Files], SetQuotaThreshold method [Files],IDiskQuotaUser interface, _win32_idiskquotauser_setquotathreshold, base.idiskquotauser_setquotathreshold, dskquota/IDiskQuotaUser::SetQuotaThreshold, fs.idiskquotauser_setquotathreshold
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
 - IDiskQuotaUser::SetQuotaThreshold
 - dskquota/IDiskQuotaUser::SetQuotaThreshold
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
 - IDiskQuotaUser.SetQuotaThreshold
---

# IDiskQuotaUser::SetQuotaThreshold


## -description

Sets the user's warning threshold value on the volume. The threshold is an arbitrary value set by the volume's quota administrator. You can use it to identify users who are approaching their hard quota limit.

## -parameters

### -param llThreshold [in]

The warning threshold value, in bytes.

### -param fWriteThrough [in]

If this value is <b>TRUE</b>, the value is written immediately to the volume's quota file. Otherwise, the value is written only to the quota user object's local memory. This value should typically be set to <b>TRUE</b>. Set it to <b>FALSE</b> when using the 
<a href="/windows/desktop/api/dskquota/nn-dskquota-idiskquotauserbatch">IDiskQuotaUserBatch</a> interface to modify multiple user quota entries at the same time.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unexpected file system error occurred.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/FileIO/disk-management-interfaces">Disk Management Interfaces</a>



<a href="/windows/desktop/FileIO/managing-disk-quotas">Disk Quotas</a>



<a href="/windows/desktop/api/dskquota/nn-dskquota-idiskquotauser">IDiskQuotaUser</a>
