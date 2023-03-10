---
UID: NF:dskquota.IDiskQuotaUser.GetAccountStatus
title: IDiskQuotaUser::GetAccountStatus (dskquota.h)
description: Retrieves the status of the user object's account.
helpviewer_keywords: ["DISKQUOTA_USER_ABLE","DISKQUOTA_USER_ACCOUNT_DELETED","DISKQUOTA_USER_ACCOUNT_INVALID","DISKQUOTA_USER_ACCOUNT_RESOLVED","DISKQUOTA_USER_ACCOUNT_UNKNOWN","DISKQUOTA_USER_ACCOUNT_UNRESOLVED","GetAccountStatus","GetAccountStatus method [Files]","GetAccountStatus method [Files]","IDiskQuotaUser interface","IDiskQuotaUser interface [Files]","GetAccountStatus method","IDiskQuotaUser.GetAccountStatus","IDiskQuotaUser::GetAccountStatus","_win32_idiskquotauser_getaccountstatus","base.idiskquotauser_getaccountstatus","dskquota/IDiskQuotaUser::GetAccountStatus","fs.idiskquotauser_getaccountstatus"]
old-location: fs\idiskquotauser_getaccountstatus.htm
tech.root: fs
ms.assetid: d4027660-beb1-45eb-9dd3-f4c12df28051
ms.date: 12/05/2018
ms.keywords: DISKQUOTA_USER_ABLE, DISKQUOTA_USER_ACCOUNT_DELETED, DISKQUOTA_USER_ACCOUNT_INVALID, DISKQUOTA_USER_ACCOUNT_RESOLVED, DISKQUOTA_USER_ACCOUNT_UNKNOWN, DISKQUOTA_USER_ACCOUNT_UNRESOLVED, GetAccountStatus, GetAccountStatus method [Files], GetAccountStatus method [Files],IDiskQuotaUser interface, IDiskQuotaUser interface [Files],GetAccountStatus method, IDiskQuotaUser.GetAccountStatus, IDiskQuotaUser::GetAccountStatus, _win32_idiskquotauser_getaccountstatus, base.idiskquotauser_getaccountstatus, dskquota/IDiskQuotaUser::GetAccountStatus, fs.idiskquotauser_getaccountstatus
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
 - IDiskQuotaUser::GetAccountStatus
 - dskquota/IDiskQuotaUser::GetAccountStatus
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
 - IDiskQuotaUser.GetAccountStatus
---

# IDiskQuotaUser::GetAccountStatus

## -description

Retrieves the status of the user object's account. User information is identified in the quota system by user security identifier (SID). This SID must resolve to a user account for the user's account name information to be retrieved.

## -parameters

### -param pdwStatus [out]

The user's account status. The status value can be one of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DISKQUOTA_USER_ACCOUNT_RESOLVED"></a><a id="diskquota_user_account_resolved"></a><dl>
<dt><b>DISKQUOTA_USER_ACCOUNT_RESOLVED</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The SID was resolved to a user account. Names are available through 
<a href="/windows/desktop/api/dskquota/nf-dskquota-idiskquotauser-getname">IDiskQuotaUser::GetName</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="DISKQUOTA_USER_ACCOUNT_UNAVAILABLE"></a><a id="diskquota_user_account_unavailable"></a><dl>
<dt><b>DISKQUOTA_USER_ACCOUNT_UNAVAILABLE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The user account is unavailable at this time. The network domain controller may not be available. Name information is not available.

</td>
</tr>
<tr>
<td width="40%"><a id="DISKQUOTA_USER_ACCOUNT_DELETED"></a><a id="diskquota_user_account_deleted"></a><dl>
<dt><b>DISKQUOTA_USER_ACCOUNT_DELETED</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The user account was deleted from the domain. Name information is not available.

</td>
</tr>
<tr>
<td width="40%"><a id="DISKQUOTA_USER_ACCOUNT_INVALID"></a><a id="diskquota_user_account_invalid"></a><dl>
<dt><b>DISKQUOTA_USER_ACCOUNT_INVALID</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The user account is invalid. Name information is not available.

</td>
</tr>
<tr>
<td width="40%"><a id="DISKQUOTA_USER_ACCOUNT_UNKNOWN"></a><a id="diskquota_user_account_unknown"></a><dl>
<dt><b>DISKQUOTA_USER_ACCOUNT_UNKNOWN</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The user account is unknown. Name information is not available.

</td>
</tr>
<tr>
<td width="40%"><a id="DISKQUOTA_USER_ACCOUNT_UNRESOLVED"></a><a id="diskquota_user_account_unresolved"></a><dl>
<dt><b>DISKQUOTA_USER_ACCOUNT_UNRESOLVED</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
The SID has not been resolved to a user account.

</td>
</tr>
</table>

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
The <i>pdwStatus</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

[Disk Management Interfaces](/windows/win32/FileIO/disk-management-interfaces)

[Disk Quotas](/windows/win32/FileIO/managing-disk-quotas)

[IDiskQuotaUser](/windows/win32/api/dskquota/nn-dskquota-idiskquotauser)
