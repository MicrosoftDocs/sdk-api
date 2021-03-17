---
UID: NF:dskquota.IDiskQuotaControl.SetDefaultQuotaThreshold
title: IDiskQuotaControl::SetDefaultQuotaThreshold (dskquota.h)
description: Modifies the default warning threshold.
helpviewer_keywords: ["IDiskQuotaControl interface [Files]","SetDefaultQuotaThreshold method","IDiskQuotaControl.SetDefaultQuotaThreshold","IDiskQuotaControl::SetDefaultQuotaThreshold","SetDefaultQuotaThreshold","SetDefaultQuotaThreshold method [Files]","SetDefaultQuotaThreshold method [Files]","IDiskQuotaControl interface","_win32_idiskquotacontrol_setdefaultquotathreshold","base.idiskquotacontrol_setdefaultquotathreshold","dskquota/IDiskQuotaControl::SetDefaultQuotaThreshold","fs.idiskquotacontrol_setdefaultquotathreshold"]
old-location: fs\idiskquotacontrol_setdefaultquotathreshold.htm
tech.root: fs
ms.assetid: a935798b-91dc-4a36-aa31-7bde68b45778
ms.date: 12/05/2018
ms.keywords: IDiskQuotaControl interface [Files],SetDefaultQuotaThreshold method, IDiskQuotaControl.SetDefaultQuotaThreshold, IDiskQuotaControl::SetDefaultQuotaThreshold, SetDefaultQuotaThreshold, SetDefaultQuotaThreshold method [Files], SetDefaultQuotaThreshold method [Files],IDiskQuotaControl interface, _win32_idiskquotacontrol_setdefaultquotathreshold, base.idiskquotacontrol_setdefaultquotathreshold, dskquota/IDiskQuotaControl::SetDefaultQuotaThreshold, fs.idiskquotacontrol_setdefaultquotathreshold
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
 - IDiskQuotaControl::SetDefaultQuotaThreshold
 - dskquota/IDiskQuotaControl::SetDefaultQuotaThreshold
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
 - IDiskQuotaControl.SetDefaultQuotaThreshold
---

# IDiskQuotaControl::SetDefaultQuotaThreshold


## -description

Modifies the default warning threshold. This threshold is applied automatically to new users of the volume.

## -parameters

### -param llThreshold [in]

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