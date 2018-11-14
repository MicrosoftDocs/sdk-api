---
UID: NF:dskquota.IDiskQuotaUser.GetName
title: IDiskQuotaUser::GetName
author: windows-sdk-content
description: Retrieves the name strings associated with a disk quota user.
old-location: fs\idiskquotauser_getname.htm
tech.root: fileio
ms.assetid: d47e064a-d121-41c3-b713-f81ff7052abf
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: GetName, GetName method [Files], GetName method [Files],IDiskQuotaUser interface, IDiskQuotaUser interface [Files],GetName method, IDiskQuotaUser.GetName, IDiskQuotaUser::GetName, _win32_idiskquotauser_getname, base.idiskquotauser_getname, dskquota/IDiskQuotaUser::GetName, fs.idiskquotauser_getname
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
 - IDiskQuotaUser.GetName
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
- IDiskQuotaUser.GetName
: 
---

# IDiskQuotaUser::GetName


## -description


Retrieves the name strings associated with a disk quota user.


## -parameters




### -param pszAccountContainer [out]

The name of the user's account container. This value can be <b>NULL</b>. For accounts without directory service information, this string is simply the domain name. For accounts with directory service information available, this string is a canonical name with the terminating object name removed.


### -param cchAccountContainer [in]

The size of the account container buffer, in characters. Ignored if <i>pszAccountContainer</i> is <b>NULL</b>.


### -param pszLogonName [out]

A pointer to the buffer to receive the name the user specified to log on the computer. This value can be <b>NULL</b>. The format of the name returned depends on whether directory service information is available.


### -param cchLogonName [in]

The size of the logon name buffer, in characters. Ignored if <i>pszLogonName</i> is <b>NULL</b>.


### -param pszDisplayName [out]

A pointer to the buffer to receive the display name for the quota user. This value can be <b>NULL</b>. If the information is not available, the string returned is of zero length.


### -param cchDisplayName [in]

The size of the display-name buffer, in characters. Ignored if <i>pszDisplayName</i> is <b>NULL</b>.


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
<dt><b>ERROR_LOCK_FAILED</b></dt>
</dl>
</td>
<td width="60%">
Failure to obtain an exclusive lock.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c1f79e2e-834b-41dc-a15f-6dd1034d021b">Disk Management Interfaces</a>



<a href="https://msdn.microsoft.com/42efbd5b-6455-4319-a76e-cdb666fc36b8">Disk Quotas</a>



<a href="https://msdn.microsoft.com/27edbebc-35b4-4f6a-87cc-d8a99782f405">IDiskQuotaUser</a>
 

 

