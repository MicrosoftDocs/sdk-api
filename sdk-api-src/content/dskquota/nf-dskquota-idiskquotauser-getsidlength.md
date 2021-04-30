---
UID: NF:dskquota.IDiskQuotaUser.GetSidLength
title: IDiskQuotaUser::GetSidLength (dskquota.h)
description: Retrieves the length of the user's security identifier (SID), in bytes.
helpviewer_keywords: ["GetSidLength","GetSidLength method [Files]","GetSidLength method [Files]","IDiskQuotaUser interface","IDiskQuotaUser interface [Files]","GetSidLength method","IDiskQuotaUser.GetSidLength","IDiskQuotaUser::GetSidLength","_win32_idiskquotauser_getsidlength","base.idiskquotauser_getsidlength","dskquota/IDiskQuotaUser::GetSidLength","fs.idiskquotauser_getsidlength"]
old-location: fs\idiskquotauser_getsidlength.htm
tech.root: fs
ms.assetid: 68fcb122-5d61-464a-99ae-d99e0d4a8117
ms.date: 12/05/2018
ms.keywords: GetSidLength, GetSidLength method [Files], GetSidLength method [Files],IDiskQuotaUser interface, IDiskQuotaUser interface [Files],GetSidLength method, IDiskQuotaUser.GetSidLength, IDiskQuotaUser::GetSidLength, _win32_idiskquotauser_getsidlength, base.idiskquotauser_getsidlength, dskquota/IDiskQuotaUser::GetSidLength, fs.idiskquotauser_getsidlength
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
 - IDiskQuotaUser::GetSidLength
 - dskquota/IDiskQuotaUser::GetSidLength
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
 - IDiskQuotaUser.GetSidLength
---

# IDiskQuotaUser::GetSidLength


## -description

Retrieves the length of the user's security identifier (SID), in bytes. Use the return value to determine the size of the destination buffer you pass to 
<a href="/windows/desktop/api/dskquota/nf-dskquota-idiskquotauser-getsid">IDiskQuotaUser::GetSid</a>.

## -parameters

### -param pdwLength [out]

The SID length, in bytes.

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
The <i>pdwLength</i> parameter is <b>NULL</b>.

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