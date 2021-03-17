---
UID: NF:dskquota.IDiskQuotaControl.GetDefaultQuotaLimit
title: IDiskQuotaControl::GetDefaultQuotaLimit (dskquota.h)
description: Retrieves the default quota limit for the volume.
helpviewer_keywords: ["GetDefaultQuotaLimit","GetDefaultQuotaLimit method [Files]","GetDefaultQuotaLimit method [Files]","IDiskQuotaControl interface","IDiskQuotaControl interface [Files]","GetDefaultQuotaLimit method","IDiskQuotaControl.GetDefaultQuotaLimit","IDiskQuotaControl::GetDefaultQuotaLimit","_win32_idiskquotacontrol_getdefaultquotalimit","base.idiskquotacontrol_getdefaultquotalimit","dskquota/IDiskQuotaControl::GetDefaultQuotaLimit","fs.idiskquotacontrol_getdefaultquotalimit"]
old-location: fs\idiskquotacontrol_getdefaultquotalimit.htm
tech.root: fs
ms.assetid: 05af5869-0c77-4078-b6af-601a7df44244
ms.date: 12/05/2018
ms.keywords: GetDefaultQuotaLimit, GetDefaultQuotaLimit method [Files], GetDefaultQuotaLimit method [Files],IDiskQuotaControl interface, IDiskQuotaControl interface [Files],GetDefaultQuotaLimit method, IDiskQuotaControl.GetDefaultQuotaLimit, IDiskQuotaControl::GetDefaultQuotaLimit, _win32_idiskquotacontrol_getdefaultquotalimit, base.idiskquotacontrol_getdefaultquotalimit, dskquota/IDiskQuotaControl::GetDefaultQuotaLimit, fs.idiskquotacontrol_getdefaultquotalimit
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
 - IDiskQuotaControl::GetDefaultQuotaLimit
 - dskquota/IDiskQuotaControl::GetDefaultQuotaLimit
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
 - IDiskQuotaControl.GetDefaultQuotaLimit
---

# IDiskQuotaControl::GetDefaultQuotaLimit


## -description

Retrieves the default quota limit for the volume. This limit is applied automatically to new users of the volume.

## -parameters

### -param pllLimit [out]

A pointer to the variable to receive the quota limit. If this value is -1, the user has an unlimited quota.

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
The <i>pllLimit</i> parameter is <b>NULL</b>.

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