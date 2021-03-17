---
UID: NF:dskquota.IDiskQuotaControl.FindUserName
title: IDiskQuotaControl::FindUserName (dskquota.h)
description: Locates a specific entry in the volume quota information.
helpviewer_keywords: ["FindUserName","FindUserName method [Files]","FindUserName method [Files]","IDiskQuotaControl interface","IDiskQuotaControl interface [Files]","FindUserName method","IDiskQuotaControl.FindUserName","IDiskQuotaControl::FindUserName","_win32_idiskquotacontrol_findusername","base.idiskquotacontrol_findusername","dskquota/IDiskQuotaControl::FindUserName","fs.idiskquotacontrol_findusername"]
old-location: fs\idiskquotacontrol_findusername.htm
tech.root: fs
ms.assetid: dae4e2d4-0293-4ee4-9687-9fed4b3a3600
ms.date: 12/05/2018
ms.keywords: FindUserName, FindUserName method [Files], FindUserName method [Files],IDiskQuotaControl interface, IDiskQuotaControl interface [Files],FindUserName method, IDiskQuotaControl.FindUserName, IDiskQuotaControl::FindUserName, _win32_idiskquotacontrol_findusername, base.idiskquotacontrol_findusername, dskquota/IDiskQuotaControl::FindUserName, fs.idiskquotacontrol_findusername
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
 - IDiskQuotaControl::FindUserName
 - dskquota/IDiskQuotaControl::FindUserName
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
 - IDiskQuotaControl.FindUserName
---

# IDiskQuotaControl::FindUserName


## -description

Locates a specific entry in the volume quota information. The user's account logon name is used as the search key.

## -parameters

### -param pszLogonName [in]

A pointer to the user's account logon name.

### -param ppUser [out]

A pointer to the 
<a href="/windows/desktop/api/dskquota/nn-dskquota-idiskquotauser">IDiskQuotaUser</a> interface pointer to the quota user object.

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
<dt><b>ERROR_INVALID_SID</b></dt>
</dl>
</td>
<td width="60%">
The SID for the user is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NONE_MAPPED</b></dt>
</dl>
</td>
<td width="60%">
There is no mapping available for the SID.

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
The <i>pUserSid</i> or <i>ppUser</i> parameter is <b>NULL</b>.

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

This method will return a user object even if there is no quota record for the user in the quota file. This is consistent with the idea of automatic user addition and default quota settings. If there is currently no quota entry for the requested user, and the user would be added to the quota file if he were to request disk space, the returned user object will have warning threshold and hard quota limits equal to the volume default settings.

## -see-also

<a href="/windows/desktop/FileIO/disk-management-interfaces">Disk Management Interfaces</a>



<a href="/windows/desktop/FileIO/managing-disk-quotas">Disk Quotas</a>



<a href="/windows/desktop/api/dskquota/nn-dskquota-idiskquotacontrol">IDiskQuotaControl</a>