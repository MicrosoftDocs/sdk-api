---
UID: NF:dskquota.IDiskQuotaControl.SetQuotaState
title: IDiskQuotaControl::SetQuotaState (dskquota.h)
description: Sets the state of the quota system.
helpviewer_keywords: ["IDiskQuotaControl interface [Files]","SetQuotaState method","IDiskQuotaControl.SetQuotaState","IDiskQuotaControl::SetQuotaState","SetQuotaState","SetQuotaState method [Files]","SetQuotaState method [Files]","IDiskQuotaControl interface","_win32_idiskquotacontrol_setquotastate","base.idiskquotacontrol_setquotastate","dskquota/IDiskQuotaControl::SetQuotaState","fs.idiskquotacontrol_setquotastate"]
old-location: fs\idiskquotacontrol_setquotastate.htm
tech.root: fs
ms.assetid: 0bbacc3c-e212-4801-95d8-1e260123665d
ms.date: 12/05/2018
ms.keywords: IDiskQuotaControl interface [Files],SetQuotaState method, IDiskQuotaControl.SetQuotaState, IDiskQuotaControl::SetQuotaState, SetQuotaState, SetQuotaState method [Files], SetQuotaState method [Files],IDiskQuotaControl interface, _win32_idiskquotacontrol_setquotastate, base.idiskquotacontrol_setquotastate, dskquota/IDiskQuotaControl::SetQuotaState, fs.idiskquotacontrol_setquotastate
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
 - IDiskQuotaControl::SetQuotaState
 - dskquota/IDiskQuotaControl::SetQuotaState
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
 - IDiskQuotaControl.SetQuotaState
---

# IDiskQuotaControl::SetQuotaState


## -description

Sets the state of the quota system.

## -parameters

### -param dwState [in]

State to be applied to the volume. Use the following macros to set the proper bits.
					

<table>
<tr>
<th>Macro</th>
<th>Enable</th>
<th>Track</th>
<th>Enforce</th>
</tr>
<tr>
<td>DISKQUOTA_SET_DISABLED</td>
<td>No</td>
<td>No</td>
<td>No</td>
</tr>
<tr>
<td>DISKQUOTA_SET_TRACKED</td>
<td>Yes</td>
<td>Yes</td>
<td>No</td>
</tr>
<tr>
<td>DISKQUOTA_SET_ENFORCED</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
</tr>
</table>

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
The <i>dwState</i> parameter is incorrect.

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

## -remarks

Not all state attributes can be modified. The enable, track, and enforce attributes can be modified.

## -see-also

<a href="/windows/desktop/FileIO/disk-management-interfaces">Disk Management Interfaces</a>



<a href="/windows/desktop/FileIO/managing-disk-quotas">Disk Quotas</a>



<a href="/windows/desktop/api/dskquota/nn-dskquota-idiskquotacontrol">IDiskQuotaControl</a>