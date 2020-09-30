---
UID: NF:dskquota.IDiskQuotaControl.GetDefaultQuotaThreshold
title: IDiskQuotaControl::GetDefaultQuotaThreshold (dskquota.h)
description: Retrieves the default quota warning threshold for the volume.
helpviewer_keywords: ["GetDefaultQuotaThreshold","GetDefaultQuotaThreshold method [Files]","GetDefaultQuotaThreshold method [Files]","IDiskQuotaControl interface","IDiskQuotaControl interface [Files]","GetDefaultQuotaThreshold method","IDiskQuotaControl.GetDefaultQuotaThreshold","IDiskQuotaControl::GetDefaultQuotaThreshold","_win32_idiskquotacontrol_getdefaultquotathreshold","base.idiskquotacontrol_getdefaultquotathreshold","dskquota/IDiskQuotaControl::GetDefaultQuotaThreshold","fs.idiskquotacontrol_getdefaultquotathreshold"]
old-location: fs\idiskquotacontrol_getdefaultquotathreshold.htm
tech.root: fs
ms.assetid: e57ec1c0-cece-4379-a695-a33c832ea7af
ms.date: 12/05/2018
ms.keywords: GetDefaultQuotaThreshold, GetDefaultQuotaThreshold method [Files], GetDefaultQuotaThreshold method [Files],IDiskQuotaControl interface, IDiskQuotaControl interface [Files],GetDefaultQuotaThreshold method, IDiskQuotaControl.GetDefaultQuotaThreshold, IDiskQuotaControl::GetDefaultQuotaThreshold, _win32_idiskquotacontrol_getdefaultquotathreshold, base.idiskquotacontrol_getdefaultquotathreshold, dskquota/IDiskQuotaControl::GetDefaultQuotaThreshold, fs.idiskquotacontrol_getdefaultquotathreshold
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
 - IDiskQuotaControl::GetDefaultQuotaThreshold
 - dskquota/IDiskQuotaControl::GetDefaultQuotaThreshold
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
 - IDiskQuotaControl.GetDefaultQuotaThreshold
---

# IDiskQuotaControl::GetDefaultQuotaThreshold


## -description

Retrieves the default quota warning threshold for the volume. This threshold is applied automatically to new users of the volume.

## -parameters

### -param pllThreshold [out]

The default warning threshold value, in bytes.

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



<a href="/windows/desktop/api/dskquota/nn-dskquota-idiskquotacontrol">IDiskQuotaControl</a>