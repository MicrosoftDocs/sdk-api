---
UID: NF:dskquota.IDiskQuotaControl.InvalidateSidNameCache
title: IDiskQuotaControl::InvalidateSidNameCache
author: windows-sdk-content
description: Invalidates the contents of the system's SID-to-name cache so subsequent requests for new user objects (IEnumDiskQuotaUsers::Next, IDiskQuotaControl::FindUserSid, and IDiskQuotaControl::FindUserName) must obtain user names from the domain controller.
old-location: fs\idiskquotacontrol_invalidatesidnamecache.htm
tech.root: fileio
ms.assetid: 9bca99e9-2dd7-4e79-ab6a-ad0e821dd9bf
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IDiskQuotaControl interface [Files],InvalidateSidNameCache method, IDiskQuotaControl.InvalidateSidNameCache, IDiskQuotaControl::InvalidateSidNameCache, InvalidateSidNameCache, InvalidateSidNameCache method [Files], InvalidateSidNameCache method [Files],IDiskQuotaControl interface, _win32_idiskquotacontrol_invalidatesidnamecache, base.idiskquotacontrol_invalidatesidnamecache, dskquota/IDiskQuotaControl::InvalidateSidNameCache, fs.idiskquotacontrol_invalidatesidnamecache
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
 - IDiskQuotaControl.InvalidateSidNameCache
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
- IDiskQuotaControl.InvalidateSidNameCache
: 
---

# IDiskQuotaControl::InvalidateSidNameCache


## -description


Invalidates the contents of the system's SID-to-name cache so subsequent requests for new user objects (<a href="https://msdn.microsoft.com/498e7c21-b18a-4d43-bbe6-9f20c2e26221">IEnumDiskQuotaUsers::Next</a>, 
<a href="https://msdn.microsoft.com/a6ce8eb3-cfa3-43b4-80ee-6dbef41f99ac">IDiskQuotaControl::FindUserSid</a>, and 
<a href="https://msdn.microsoft.com/dae4e2d4-0293-4ee4-9687-9fed4b3a3600">IDiskQuotaControl::FindUserName</a>) must obtain user names from the domain controller. As names are obtained, they are cached.


## -parameters






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
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The SID-to-name cache is not available or could not be exclusively locked.

</td>
</tr>
</table>
 




## -remarks



In general, there is no reason to call this method. It is included to provide a method for programmatically refreshing the entire SID-to-name cache.




## -see-also




<a href="https://msdn.microsoft.com/c1f79e2e-834b-41dc-a15f-6dd1034d021b">Disk Management Interfaces</a>



<a href="https://msdn.microsoft.com/42efbd5b-6455-4319-a76e-cdb666fc36b8">Disk Quotas</a>



<a href="https://msdn.microsoft.com/fc9add5a-c9ef-462d-8125-128d48018717">IDiskQuotaControl</a>
 

 

