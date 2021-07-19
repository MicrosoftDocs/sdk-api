---
UID: NF:dskquota.IDiskQuotaControl.InvalidateSidNameCache
title: IDiskQuotaControl::InvalidateSidNameCache (dskquota.h)
description: Invalidates the contents of the system's SID-to-name cache so subsequent requests for new user objects (IEnumDiskQuotaUsers::Next, IDiskQuotaControl::FindUserSid, and IDiskQuotaControl::FindUserName) must obtain user names from the domain controller.
helpviewer_keywords: ["IDiskQuotaControl interface [Files]","InvalidateSidNameCache method","IDiskQuotaControl.InvalidateSidNameCache","IDiskQuotaControl::InvalidateSidNameCache","InvalidateSidNameCache","InvalidateSidNameCache method [Files]","InvalidateSidNameCache method [Files]","IDiskQuotaControl interface","_win32_idiskquotacontrol_invalidatesidnamecache","base.idiskquotacontrol_invalidatesidnamecache","dskquota/IDiskQuotaControl::InvalidateSidNameCache","fs.idiskquotacontrol_invalidatesidnamecache"]
old-location: fs\idiskquotacontrol_invalidatesidnamecache.htm
tech.root: fs
ms.assetid: 9bca99e9-2dd7-4e79-ab6a-ad0e821dd9bf
ms.date: 12/05/2018
ms.keywords: IDiskQuotaControl interface [Files],InvalidateSidNameCache method, IDiskQuotaControl.InvalidateSidNameCache, IDiskQuotaControl::InvalidateSidNameCache, InvalidateSidNameCache, InvalidateSidNameCache method [Files], InvalidateSidNameCache method [Files],IDiskQuotaControl interface, _win32_idiskquotacontrol_invalidatesidnamecache, base.idiskquotacontrol_invalidatesidnamecache, dskquota/IDiskQuotaControl::InvalidateSidNameCache, fs.idiskquotacontrol_invalidatesidnamecache
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
 - IDiskQuotaControl::InvalidateSidNameCache
 - dskquota/IDiskQuotaControl::InvalidateSidNameCache
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
 - IDiskQuotaControl.InvalidateSidNameCache
---

# IDiskQuotaControl::InvalidateSidNameCache


## -description

Invalidates the contents of the system's SID-to-name cache so subsequent requests for new user objects (<a href="/windows/desktop/api/dskquota/nf-dskquota-ienumdiskquotausers-next">IEnumDiskQuotaUsers::Next</a>, 
<a href="/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-findusersid">IDiskQuotaControl::FindUserSid</a>, and 
<a href="/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-findusername">IDiskQuotaControl::FindUserName</a>) must obtain user names from the domain controller. As names are obtained, they are cached.



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

<a href="/windows/desktop/FileIO/disk-management-interfaces">Disk Management Interfaces</a>



<a href="/windows/desktop/FileIO/managing-disk-quotas">Disk Quotas</a>



<a href="/windows/desktop/api/dskquota/nn-dskquota-idiskquotacontrol">IDiskQuotaControl</a>
