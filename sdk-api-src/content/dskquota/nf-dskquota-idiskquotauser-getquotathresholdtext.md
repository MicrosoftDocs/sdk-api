---
UID: NF:dskquota.IDiskQuotaUser.GetQuotaThresholdText
title: IDiskQuotaUser::GetQuotaThresholdText (dskquota.h)
description: Retrieves the user's warning threshold for the volume.
helpviewer_keywords: ["GetQuotaThresholdText","GetQuotaThresholdText method [Files]","GetQuotaThresholdText method [Files]","IDiskQuotaUser interface","IDiskQuotaUser interface [Files]","GetQuotaThresholdText method","IDiskQuotaUser.GetQuotaThresholdText","IDiskQuotaUser::GetQuotaThresholdText","_win32_idiskquotauser_getquotathresholdtext","base.idiskquotauser_getquotathresholdtext","dskquota/IDiskQuotaUser::GetQuotaThresholdText","fs.idiskquotauser_getquotathresholdtext"]
old-location: fs\idiskquotauser_getquotathresholdtext.htm
tech.root: fs
ms.assetid: 19391a9e-e64c-4e6f-8b52-efe59ed45ae5
ms.date: 12/05/2018
ms.keywords: GetQuotaThresholdText, GetQuotaThresholdText method [Files], GetQuotaThresholdText method [Files],IDiskQuotaUser interface, IDiskQuotaUser interface [Files],GetQuotaThresholdText method, IDiskQuotaUser.GetQuotaThresholdText, IDiskQuotaUser::GetQuotaThresholdText, _win32_idiskquotauser_getquotathresholdtext, base.idiskquotauser_getquotathresholdtext, dskquota/IDiskQuotaUser::GetQuotaThresholdText, fs.idiskquotauser_getquotathresholdtext
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
 - IDiskQuotaUser::GetQuotaThresholdText
 - dskquota/IDiskQuotaUser::GetQuotaThresholdText
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
 - IDiskQuotaUser.GetQuotaThresholdText
---

# IDiskQuotaUser::GetQuotaThresholdText


## -description

Retrieves the user's warning threshold for the volume. This threshold is expressed as a text string, for example "10.5 MB". If the user's threshold is unlimited, the string returned is "No Limit" (localized). If the destination buffer is too small, the string is truncated to fit the buffer.

## -parameters

### -param pszText [out]

The text string.

### -param cchText [in]

The size of the destination buffer, in characters.

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
The <i>pszText</i> parameter is <b>NULL</b>.

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