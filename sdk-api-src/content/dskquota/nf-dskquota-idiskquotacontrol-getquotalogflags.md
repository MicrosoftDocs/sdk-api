---
UID: NF:dskquota.IDiskQuotaControl.GetQuotaLogFlags
title: IDiskQuotaControl::GetQuotaLogFlags (dskquota.h)
description: Retrieves the flags that control the logging of user-related quota events on the volume.
helpviewer_keywords: ["GetQuotaLogFlags","GetQuotaLogFlags method [Files]","GetQuotaLogFlags method [Files]","IDiskQuotaControl interface","IDiskQuotaControl interface [Files]","GetQuotaLogFlags method","IDiskQuotaControl.GetQuotaLogFlags","IDiskQuotaControl::GetQuotaLogFlags","_win32_idiskquotacontrol_getquotalogflags","base.idiskquotacontrol_getquotalogflags","dskquota/IDiskQuotaControl::GetQuotaLogFlags","fs.idiskquotacontrol_getquotalogflags"]
old-location: fs\idiskquotacontrol_getquotalogflags.htm
tech.root: fs
ms.assetid: 79ba4f8a-9f89-4c15-9d17-b61960d12b62
ms.date: 12/05/2018
ms.keywords: GetQuotaLogFlags, GetQuotaLogFlags method [Files], GetQuotaLogFlags method [Files],IDiskQuotaControl interface, IDiskQuotaControl interface [Files],GetQuotaLogFlags method, IDiskQuotaControl.GetQuotaLogFlags, IDiskQuotaControl::GetQuotaLogFlags, _win32_idiskquotacontrol_getquotalogflags, base.idiskquotacontrol_getquotalogflags, dskquota/IDiskQuotaControl::GetQuotaLogFlags, fs.idiskquotacontrol_getquotalogflags
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
 - IDiskQuotaControl::GetQuotaLogFlags
 - dskquota/IDiskQuotaControl::GetQuotaLogFlags
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
 - IDiskQuotaControl.GetQuotaLogFlags
---

# IDiskQuotaControl::GetQuotaLogFlags


## -description

Retrieves the flags that control the logging of user-related quota events on the volume. Logging makes an entry in the volume server's event log.

## -parameters

### -param pdwFlags [out]

The volume's quota logging flags. Use the following macros to retrieve the contents of the flag value.

<table>
<tr>
<th>Macro</th>
<th>Description</th>
</tr>
<tr>
<td>DISKQUOTA_IS_LOGGED_USER_LIMIT</td>
<td>If set, an event log entry will be created when the user exceeds his assigned hard quota limit.</td>
</tr>
<tr>
<td>DISKQUOTA_IS_LOGGED_USER_THRESHOLD</td>
<td>If set, an event log entry will be created when the user exceeds his assigned warning threshold.</td>
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
The <i>pdwFlags</i> parameter is incorrect.

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