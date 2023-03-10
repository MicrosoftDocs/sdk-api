---
UID: NF:dskquota.IDiskQuotaControl.AddUserName
title: IDiskQuotaControl::AddUserName (dskquota.h)
description: Adds a new quota entry on the volume for the specified user. The user is identified by domain and account name.
helpviewer_keywords: ["AddUserName","AddUserName method [Files]","AddUserName method [Files]","IDiskQuotaControl interface","DISKQUOTA_USERNAME_RESOLVE_ASYNC","DISKQUOTA_USERNAME_RESOLVE_NONE","DISKQUOTA_USERNAME_RESOLVE_SYNC","IDiskQuotaControl interface [Files]","AddUserName method","IDiskQuotaControl.AddUserName","IDiskQuotaControl::AddUserName","_win32_idiskquotacontrol_addusername","base.idiskquotacontrol_addusername","dskquota/IDiskQuotaControl::AddUserName","fs.idiskquotacontrol_addusername"]
old-location: fs\idiskquotacontrol_addusername.htm
tech.root: fs
ms.assetid: 306120e8-642a-439d-839c-944cb7fd7ee2
ms.date: 12/05/2018
ms.keywords: AddUserName, AddUserName method [Files], AddUserName method [Files],IDiskQuotaControl interface, DISKQUOTA_USERNAME_RESOLVE_ASYNC, DISKQUOTA_USERNAME_RESOLVE_NONE, DISKQUOTA_USERNAME_RESOLVE_SYNC, IDiskQuotaControl interface [Files],AddUserName method, IDiskQuotaControl.AddUserName, IDiskQuotaControl::AddUserName, _win32_idiskquotacontrol_addusername, base.idiskquotacontrol_addusername, dskquota/IDiskQuotaControl::AddUserName, fs.idiskquotacontrol_addusername
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
 - IDiskQuotaControl::AddUserName
 - dskquota/IDiskQuotaControl::AddUserName
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
 - IDiskQuotaControl.AddUserName
---

# IDiskQuotaControl::AddUserName


## -description

Adds a new quota entry on the volume for the specified user. The user is identified by domain and account name.

## -parameters

### -param pszLogonName [in]

The user's account logon name string.

### -param fNameResolution [in]

Indicates how the user account information is to be obtained. The volume's quota information identifies users by SID. The user account information (such as container, logon name, and display name) must be obtained from the network domain controller, or the local computer if it is not on a network. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DISKQUOTA_USERNAME_RESOLVE_ASYNC"></a><a id="diskquota_username_resolve_async"></a><dl>
<dt><b>DISKQUOTA_USERNAME_RESOLVE_ASYNC</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Resolve user account information asynchronously. 
<b>AddUserName</b> returns immediately. The caller must implement the 
<a href="/windows/desktop/api/dskquota/nn-dskquota-idiskquotaevents">IDiskQuotaEvents</a> interface to receive notification when the information is available. If the information was cached during a previous request, notification occurs as soon as the object is serviced. Otherwise, the method obtains the information from the network domain controller, then notifies 
<b>IDiskQuotaEvents</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="DISKQUOTA_USERNAME_RESOLVE_NONE"></a><a id="diskquota_username_resolve_none"></a><dl>
<dt><b>DISKQUOTA_USERNAME_RESOLVE_NONE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Do not resolve user account information.

</td>
</tr>
<tr>
<td width="40%"><a id="DISKQUOTA_USERNAME_RESOLVE_SYNC"></a><a id="diskquota_username_resolve_sync"></a><dl>
<dt><b>DISKQUOTA_USERNAME_RESOLVE_SYNC</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Resolve user account information synchronously. 
<b>AddUserName</b> returns when the information is resolved. If the information exists in the disk quota SID cache, it is returned immediately. Otherwise, the method must locate the information. This can take several seconds.

</td>
</tr>
</table>

### -param ppUser [out]

A pointer to the 
<a href="/windows/desktop/api/dskquota/nn-dskquota-idiskquotauser">IDiskQuotaUser</a> interface pointer to the newly created quota user object.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
User already exists. Not added.

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
<dt><b>ERROR_USER_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
The specified user name is unknown.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
A pointer parameter is <b>NULL</b>.

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

The NTFS file system automatically creates a user quota entry when a user first writes to the volume. Entries that are created automatically are assigned the default warning threshold and hard quota limit values for the volume. This method allows you to create a user quota entry before a user has written information to the volume. Therefore, you can pre-assign a warning threshold or hard quota limit value different than the volume default settings.

## -see-also

<a href="/windows/desktop/FileIO/disk-management-interfaces">Disk Management Interfaces</a>



<a href="/windows/desktop/FileIO/managing-disk-quotas">Disk Quotas</a>



<a href="/windows/desktop/api/dskquota/nn-dskquota-idiskquotacontrol">IDiskQuotaControl</a>