---
UID: NF:dskquota.IDiskQuotaControl.FindUserName
title: IDiskQuotaControl::FindUserName
author: windows-sdk-content
description: Locates a specific entry in the volume quota information.
old-location: fs\idiskquotacontrol_findusername.htm
tech.root: fileio
ms.assetid: dae4e2d4-0293-4ee4-9687-9fed4b3a3600
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: FindUserName, FindUserName method [Files], FindUserName method [Files],IDiskQuotaControl interface, IDiskQuotaControl interface [Files],FindUserName method, IDiskQuotaControl.FindUserName, IDiskQuotaControl::FindUserName, _win32_idiskquotacontrol_findusername, base.idiskquotacontrol_findusername, dskquota/IDiskQuotaControl::FindUserName, fs.idiskquotacontrol_findusername
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
 - IDiskQuotaControl.FindUserName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiskQuotaControl::FindUserName


## -description


Locates a specific entry in the volume quota information. The user's account logon name is used as the search key.


## -parameters




### -param pszLogonName [in]

A pointer to the user's account logon name.


### -param ppUser [out]

A pointer to the 
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




<a href="https://msdn.microsoft.com/c1f79e2e-834b-41dc-a15f-6dd1034d021b">Disk Management Interfaces</a>



<a href="https://msdn.microsoft.com/42efbd5b-6455-4319-a76e-cdb666fc36b8">Disk Quotas</a>



<a href="https://msdn.microsoft.com/fc9add5a-c9ef-462d-8125-128d48018717">IDiskQuotaControl</a>
 

 

