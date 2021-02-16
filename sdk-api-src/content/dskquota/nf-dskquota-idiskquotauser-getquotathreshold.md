---
UID: NF:dskquota.IDiskQuotaUser.GetQuotaThreshold
title: IDiskQuotaUser::GetQuotaThreshold (dskquota.h)
description: Retrieves the user's warning threshold value on the volume.
helpviewer_keywords: ["GetQuotaThreshold","GetQuotaThreshold method [Files]","GetQuotaThreshold method [Files]","IDiskQuotaUser interface","IDiskQuotaUser interface [Files]","GetQuotaThreshold method","IDiskQuotaUser.GetQuotaThreshold","IDiskQuotaUser::GetQuotaThreshold","_win32_idiskquotauser_getquotathreshold","base.idiskquotauser_getquotathreshold","dskquota/IDiskQuotaUser::GetQuotaThreshold","fs.idiskquotauser_getquotathreshold"]
old-location: fs\idiskquotauser_getquotathreshold.htm
tech.root: fs
ms.assetid: 58b925f3-b40a-4fab-86c6-725e04e6f721
ms.date: 12/05/2018
ms.keywords: GetQuotaThreshold, GetQuotaThreshold method [Files], GetQuotaThreshold method [Files],IDiskQuotaUser interface, IDiskQuotaUser interface [Files],GetQuotaThreshold method, IDiskQuotaUser.GetQuotaThreshold, IDiskQuotaUser::GetQuotaThreshold, _win32_idiskquotauser_getquotathreshold, base.idiskquotauser_getquotathreshold, dskquota/IDiskQuotaUser::GetQuotaThreshold, fs.idiskquotauser_getquotathreshold
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
 - IDiskQuotaUser::GetQuotaThreshold
 - dskquota/IDiskQuotaUser::GetQuotaThreshold
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
 - IDiskQuotaUser.GetQuotaThreshold
---

# IDiskQuotaUser::GetQuotaThreshold


## -description

Retrieves the user's warning threshold value on the volume. The threshold is an arbitrary value set by the volume's quota administrator. You can use it to identify users who are approaching their hard quota limit.

## -parameters

### -param pllThreshold [out]

The warning threshold value.

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
<dt><b>ERROR_LOCK_FAILED</b></dt>
</dl>
</td>
<td width="60%">
Failure to obtain an exclusive lock.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pllThreshold</i> parameter is <b>NULL</b>.

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

## -see-also

<a href="/windows/desktop/FileIO/disk-management-interfaces">Disk Management Interfaces</a>



<a href="/windows/desktop/FileIO/managing-disk-quotas">Disk Quotas</a>



<a href="/windows/desktop/api/dskquota/nn-dskquota-idiskquotauser">IDiskQuotaUser</a>