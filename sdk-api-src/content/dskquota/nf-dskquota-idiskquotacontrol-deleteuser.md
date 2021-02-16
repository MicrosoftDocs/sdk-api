---
UID: NF:dskquota.IDiskQuotaControl.DeleteUser
title: IDiskQuotaControl::DeleteUser (dskquota.h)
description: Removes a user entry from the volume quota information file.
helpviewer_keywords: ["DeleteUser","DeleteUser method [Files]","DeleteUser method [Files]","IDiskQuotaControl interface","IDiskQuotaControl interface [Files]","DeleteUser method","IDiskQuotaControl.DeleteUser","IDiskQuotaControl::DeleteUser","_win32_idiskquotacontrol_deleteuser","base.idiskquotacontrol_deleteuser","dskquota/IDiskQuotaControl::DeleteUser","fs.idiskquotacontrol_deleteuser"]
old-location: fs\idiskquotacontrol_deleteuser.htm
tech.root: fs
ms.assetid: c7356f56-4cbb-40ed-9457-3818a3b47732
ms.date: 12/05/2018
ms.keywords: DeleteUser, DeleteUser method [Files], DeleteUser method [Files],IDiskQuotaControl interface, IDiskQuotaControl interface [Files],DeleteUser method, IDiskQuotaControl.DeleteUser, IDiskQuotaControl::DeleteUser, _win32_idiskquotacontrol_deleteuser, base.idiskquotacontrol_deleteuser, dskquota/IDiskQuotaControl::DeleteUser, fs.idiskquotacontrol_deleteuser
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
 - IDiskQuotaControl::DeleteUser
 - dskquota/IDiskQuotaControl::DeleteUser
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
 - IDiskQuotaControl.DeleteUser
---

# IDiskQuotaControl::DeleteUser


## -description

Removes a user entry from the volume quota information file, if the user's charged quota amount is zero (0) bytes.

## -parameters

### -param pUser [in]

A pointer to the 
<a href="/windows/desktop/api/dskquota/nn-dskquota-idiskquotauser">IDiskQuotaUser</a> interface of the user whose quota record is marked for deletion.

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
<dt><b>ERROR_FILE_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The user owns files on the volume.

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
The <i>pUser</i> parameter is <b>NULL</b>.

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

This method does not actually remove the quota entry from the volume. It marks the entry for deletion. The NTFS file system performs the actual deletion at a later time. Following a call to <b>IDiskQuotaControl::DeleteUser</b>, the 
<a href="/windows/desktop/api/dskquota/nn-dskquota-idiskquotauser">IDiskQuotaUser</a> interface is still active. This method does not delete the user object from memory. To release the user object, call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a>.

## -see-also

<a href="/windows/desktop/FileIO/disk-management-interfaces">Disk Management Interfaces</a>



<a href="/windows/desktop/FileIO/managing-disk-quotas">Disk Quotas</a>



<a href="/windows/desktop/api/dskquota/nn-dskquota-idiskquotacontrol">IDiskQuotaControl</a>