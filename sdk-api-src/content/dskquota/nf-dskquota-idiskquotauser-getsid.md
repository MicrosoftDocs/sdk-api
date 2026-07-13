---
UID: NF:dskquota.IDiskQuotaUser.GetSid
title: IDiskQuotaUser::GetSid (dskquota.h)
description: Retrieves the user's security identifier (SID). (IDiskQuotaUser.GetSid)
helpviewer_keywords: ["GetSid","GetSid method [Files]","GetSid method [Files]","IDiskQuotaUser interface","IDiskQuotaUser interface [Files]","GetSid method","IDiskQuotaUser.GetSid","IDiskQuotaUser::GetSid","_win32_idiskquotauser_getsid","base.idiskquotauser_getsid","dskquota/IDiskQuotaUser::GetSid","fs.idiskquotauser_getsid"]
old-location: fs\idiskquotauser_getsid.htm
tech.root: fs
ms.assetid: 1718b5eb-2385-4e0f-a6af-99a5ef73e55d
ms.date: 12/05/2018
ms.keywords: GetSid, GetSid method [Files], GetSid method [Files],IDiskQuotaUser interface, IDiskQuotaUser interface [Files],GetSid method, IDiskQuotaUser.GetSid, IDiskQuotaUser::GetSid, _win32_idiskquotauser_getsid, base.idiskquotauser_getsid, dskquota/IDiskQuotaUser::GetSid, fs.idiskquotauser_getsid
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
 - IDiskQuotaUser::GetSid
 - dskquota/IDiskQuotaUser::GetSid
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
 - IDiskQuotaUser.GetSid
---

# IDiskQuotaUser::GetSid


## -description

Retrieves the user's security identifier (SID).

## -parameters

### -param pbSidBuffer [out]

The SID.

### -param cbSidBuffer [in]

The size of the buffer, in bytes. Use the 
<a href="/windows/desktop/api/dskquota/nf-dskquota-idiskquotauser-getsidlength">IDiskQuotaUser::GetSidLength</a> method to obtain the required size for the buffer.

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
The <i>pbSidBuffer</i> parameter is <b>NULL</b>.

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
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
Insufficient destination buffer size.

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

<a href="/windows/desktop/FileIO/disk-management-interfaces">Disk Management Interfaces</a>



<a href="/windows/desktop/FileIO/managing-disk-quotas">Disk Quotas</a>



<a href="/windows/desktop/api/dskquota/nn-dskquota-idiskquotauser">IDiskQuotaUser</a>
