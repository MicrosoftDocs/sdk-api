---
UID: NF:dskquota.IDiskQuotaControl.GetDefaultQuotaLimitText
title: IDiskQuotaControl::GetDefaultQuotaLimitText (dskquota.h)
description: Retrieves the default quota limit for the volume. The limit is expressed as a text string; for example, 10.5 MB.
helpviewer_keywords: ["GetDefaultQuotaLimitText","GetDefaultQuotaLimitText method [Files]","GetDefaultQuotaLimitText method [Files]","IDiskQuotaControl interface","IDiskQuotaControl interface [Files]","GetDefaultQuotaLimitText method","IDiskQuotaControl.GetDefaultQuotaLimitText","IDiskQuotaControl::GetDefaultQuotaLimitText","_win32_idiskquotacontrol_getdefaultquotalimittext","base.idiskquotacontrol_getdefaultquotalimittext","dskquota/IDiskQuotaControl::GetDefaultQuotaLimitText","fs.idiskquotacontrol_getdefaultquotalimittext"]
old-location: fs\idiskquotacontrol_getdefaultquotalimittext.htm
tech.root: fs
ms.assetid: a39d457c-9a6f-4d57-a91f-878fcb96916e
ms.date: 12/05/2018
ms.keywords: GetDefaultQuotaLimitText, GetDefaultQuotaLimitText method [Files], GetDefaultQuotaLimitText method [Files],IDiskQuotaControl interface, IDiskQuotaControl interface [Files],GetDefaultQuotaLimitText method, IDiskQuotaControl.GetDefaultQuotaLimitText, IDiskQuotaControl::GetDefaultQuotaLimitText, _win32_idiskquotacontrol_getdefaultquotalimittext, base.idiskquotacontrol_getdefaultquotalimittext, dskquota/IDiskQuotaControl::GetDefaultQuotaLimitText, fs.idiskquotacontrol_getdefaultquotalimittext
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
 - IDiskQuotaControl::GetDefaultQuotaLimitText
 - dskquota/IDiskQuotaControl::GetDefaultQuotaLimitText
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
 - IDiskQuotaControl.GetDefaultQuotaLimitText
---

# IDiskQuotaControl::GetDefaultQuotaLimitText


## -description

Retrieves the default quota limit for the volume. The limit is expressed as a text string; for example, 10.5 MB. This limit is applied automatically to new users of the volume.

## -parameters

### -param pszText [out]

The text string. If the volume has no limit, the string returned is "No Limit" (localized). If the buffer is too small, the string is truncated to fit the buffer.

### -param cchText [in]

The size of the buffer, in characters.

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



<a href="/windows/desktop/api/dskquota/nn-dskquota-idiskquotacontrol">IDiskQuotaControl</a>