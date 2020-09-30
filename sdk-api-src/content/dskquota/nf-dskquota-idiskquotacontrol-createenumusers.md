---
UID: NF:dskquota.IDiskQuotaControl.CreateEnumUsers
title: IDiskQuotaControl::CreateEnumUsers (dskquota.h)
description: Creates an enumerator object for enumerating quota users on the volume.
helpviewer_keywords: ["CreateEnumUsers","CreateEnumUsers method [Files]","CreateEnumUsers method [Files]","IDiskQuotaControl interface","DISKQUOTA_USERNAME_RESOLVE_ASYNC","DISKQUOTA_USERNAME_RESOLVE_NONE","DISKQUOTA_USERNAME_RESOLVE_SYNC","IDiskQuotaControl interface [Files]","CreateEnumUsers method","IDiskQuotaControl.CreateEnumUsers","IDiskQuotaControl::CreateEnumUsers","_win32_idiskquotacontrol_createenumusers","base.idiskquotacontrol_createenumusers","dskquota/IDiskQuotaControl::CreateEnumUsers","fs.idiskquotacontrol_createenumusers"]
old-location: fs\idiskquotacontrol_createenumusers.htm
tech.root: fs
ms.assetid: a29e1955-80e2-442d-9565-c885006be565
ms.date: 12/05/2018
ms.keywords: CreateEnumUsers, CreateEnumUsers method [Files], CreateEnumUsers method [Files],IDiskQuotaControl interface, DISKQUOTA_USERNAME_RESOLVE_ASYNC, DISKQUOTA_USERNAME_RESOLVE_NONE, DISKQUOTA_USERNAME_RESOLVE_SYNC, IDiskQuotaControl interface [Files],CreateEnumUsers method, IDiskQuotaControl.CreateEnumUsers, IDiskQuotaControl::CreateEnumUsers, _win32_idiskquotacontrol_createenumusers, base.idiskquotacontrol_createenumusers, dskquota/IDiskQuotaControl::CreateEnumUsers, fs.idiskquotacontrol_createenumusers
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
 - IDiskQuotaControl::CreateEnumUsers
 - dskquota/IDiskQuotaControl::CreateEnumUsers
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
 - IDiskQuotaControl.CreateEnumUsers
---

# IDiskQuotaControl::CreateEnumUsers


## -description

Creates an enumerator object for enumerating quota users on the volume. The newly created object implements the 
<a href="/windows/desktop/api/dskquota/nn-dskquota-ienumdiskquotausers">IEnumDiskQuotaUsers</a> interface.

## -parameters

### -param rgpUserSids [in]

An array of security identifier (SID) pointers representing the user objects to be included in the enumeration. If this value is <b>NULL</b>, all user entries are enumerated.

### -param cpSids [in]

The number of items in the <i>rgpUserSids</i> array. Ignored if <i>rgpUserSids</i> is <b>NULL</b>.

### -param fNameResolution [in]

Indicates how the user account information is to be obtained. The volume's quota information identifies users by SID. The user account information (such as domain name, account name, and full name) must be obtained from the network domain controller, or the local computer if it is not on a network. This parameter can be one of the following values.

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
Resolve user account information asynchronously. The 
<a href="/windows/desktop/api/dskquota/nf-dskquota-ienumdiskquotausers-next">IEnumDiskQuotaUsers::Next</a> method returns immediately. The caller must implement the 
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
Resolve user account information synchronously. The 
<a href="/windows/desktop/api/dskquota/nf-dskquota-ienumdiskquotausers-next">IEnumDiskQuotaUsers::Next</a> method returns when the information is resolved. If the information exists in the disk quota SID cache, it is returned immediately. Otherwise, the method must locate the information. This can take several seconds.

</td>
</tr>
</table>

### -param ppEnum [out]

A pointer to a pointer to the 
<a href="/windows/desktop/api/dskquota/nn-dskquota-ienumdiskquotausers">IEnumDiskQuotaUsers</a> enumerator.

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
The DiskQuotaControl object is not initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppEnum</i> parameter is <b>NULL</b>.

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