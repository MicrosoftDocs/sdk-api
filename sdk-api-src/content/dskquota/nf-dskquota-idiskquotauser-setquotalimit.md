---
UID: NF:dskquota.IDiskQuotaUser.SetQuotaLimit
title: IDiskQuotaUser::SetQuotaLimit (dskquota.h)
description: Sets the user's quota limit value on the volume.
helpviewer_keywords: ["IDiskQuotaUser interface [Files]","SetQuotaLimit method","IDiskQuotaUser.SetQuotaLimit","IDiskQuotaUser::SetQuotaLimit","SetQuotaLimit","SetQuotaLimit method [Files]","SetQuotaLimit method [Files]","IDiskQuotaUser interface","_win32_idiskquotauser_setquotalimit","base.idiskquotauser_setquotalimit","dskquota/IDiskQuotaUser::SetQuotaLimit","fs.idiskquotauser_setquotalimit"]
old-location: fs\idiskquotauser_setquotalimit.htm
tech.root: fs
ms.assetid: f7c99415-685b-4a21-ac7b-68f4816aafb0
ms.date: 12/05/2018
ms.keywords: IDiskQuotaUser interface [Files],SetQuotaLimit method, IDiskQuotaUser.SetQuotaLimit, IDiskQuotaUser::SetQuotaLimit, SetQuotaLimit, SetQuotaLimit method [Files], SetQuotaLimit method [Files],IDiskQuotaUser interface, _win32_idiskquotauser_setquotalimit, base.idiskquotauser_setquotalimit, dskquota/IDiskQuotaUser::SetQuotaLimit, fs.idiskquotauser_setquotalimit
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
 - IDiskQuotaUser::SetQuotaLimit
 - dskquota/IDiskQuotaUser::SetQuotaLimit
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
 - IDiskQuotaUser.SetQuotaLimit
---

# IDiskQuotaUser::SetQuotaLimit


## -description

Sets the user's quota limit value on the volume. The limit is set as the maximum amount of disk space available to the volume user.

## -parameters

### -param llLimit [in]

The quota limit, in bytes. If this value is -1, the user has an unlimited quota.

### -param fWriteThrough [in]

If this value is <b>TRUE</b>, the value is written immediately to the volume's quota file. Otherwise, the value is written only to the quota user object's local memory. This value should typically be set to <b>TRUE</b>. Set it to <b>FALSE</b> when using the 
<a href="/windows/desktop/api/dskquota/nn-dskquota-idiskquotauserbatch">IDiskQuotaUserBatch</a> interface to modify multiple user quota entries at once.

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
