---
UID: NF:dskquota.IDiskQuotaControl.FindUserSid
title: IDiskQuotaControl::FindUserSid
author: windows-sdk-content
description: Locates a specific user entry in the volume quota information.
old-location: fs\idiskquotacontrol_findusersid.htm
tech.root: fileio
ms.assetid: a6ce8eb3-cfa3-43b4-80ee-6dbef41f99ac
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: DISKQUOTA_USERNAME_RESOLVE_ASYNC, DISKQUOTA_USERNAME_RESOLVE_NONE, DISKQUOTA_USERNAME_RESOLVE_SYNC, FindUserSid, FindUserSid method [Files], FindUserSid method [Files],IDiskQuotaControl interface, IDiskQuotaControl interface [Files],FindUserSid method, IDiskQuotaControl.FindUserSid, IDiskQuotaControl::FindUserSid, _win32_idiskquotacontrol_findusersid, base.idiskquotacontrol_findusersid, dskquota/IDiskQuotaControl::FindUserSid, fs.idiskquotacontrol_findusersid
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dskquota.dll
api_name:
 - IDiskQuotaControl.FindUserSid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dskquota.h
: 
- IDiskQuotaControl.FindUserSid
: 
---

# IDiskQuotaControl::FindUserSid


## -description


Locates a specific user entry in the volume quota information. The user's security identifier (SID) is used as the search key.


## -parameters




### -param pUserSid [in]

A pointer to the user's SID.


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
Resolve user account information asynchronously. 
<b>FindUserSid</b> returns immediately. The caller must implement the 
<a href="https://msdn.microsoft.com/4b5dcb1f-8edb-4fcb-94ea-2a627667071e">IDiskQuotaEvents</a> interface to receive notification when the information is available. If the information was cached during a previous request, notification occurs as soon as the object is serviced. Otherwise, the method obtains the information from the network domain controller, then notifies 
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
<b>FindUserSid</b> returns when the information has been resolved. If the information exists in the disk quota SID cache, it is returned immediately. Otherwise, the method must locate the information. This can take several seconds.

</td>
</tr>
</table>
 


### -param ppUser [out]

Pointer to receive the 
<a href="https://msdn.microsoft.com/27edbebc-35b4-4f6a-87cc-d8a99782f405">IDiskQuotaUser</a> interface pointer to the quota user object.


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




<a href="https://msdn.microsoft.com/c1f79e2e-834b-41dc-a15f-6dd1034d021b">Disk Management Interfaces</a>



<a href="https://msdn.microsoft.com/42efbd5b-6455-4319-a76e-cdb666fc36b8">Disk Quotas</a>



<a href="https://msdn.microsoft.com/fc9add5a-c9ef-462d-8125-128d48018717">IDiskQuotaControl</a>
 

 

