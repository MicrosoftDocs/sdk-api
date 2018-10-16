---
UID: NF:dskquota.IDiskQuotaControl.DeleteUser
title: IDiskQuotaControl::DeleteUser
author: windows-sdk-content
description: Removes a user entry from the volume quota information file.
old-location: fs\idiskquotacontrol_deleteuser.htm
tech.root: fileio
ms.assetid: c7356f56-4cbb-40ed-9457-3818a3b47732
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: DeleteUser, DeleteUser method [Files], DeleteUser method [Files],IDiskQuotaControl interface, IDiskQuotaControl interface [Files],DeleteUser method, IDiskQuotaControl.DeleteUser, IDiskQuotaControl::DeleteUser, _win32_idiskquotacontrol_deleteuser, base.idiskquotacontrol_deleteuser, dskquota/IDiskQuotaControl::DeleteUser, fs.idiskquotacontrol_deleteuser
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dskquota.dll
api_name:
 - IDiskQuotaControl.DeleteUser
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiskQuotaControl::DeleteUser


## -description


Removes a user entry from the volume quota information file, if the user's charged quota amount is zero (0) bytes.


## -parameters




### -param pUser [in]

A pointer to the 
<a href="https://msdn.microsoft.com/27edbebc-35b4-4f6a-87cc-d8a99782f405">IDiskQuotaUser</a> interface of the user whose quota record is marked for deletion.


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
<a href="https://msdn.microsoft.com/27edbebc-35b4-4f6a-87cc-d8a99782f405">IDiskQuotaUser</a> interface is still active. This method does not delete the user object from memory. To release the user object, call <a href="_com_iunknown_release">IUnknown::Release</a>.




## -see-also




<a href="https://msdn.microsoft.com/c1f79e2e-834b-41dc-a15f-6dd1034d021b">Disk Management Interfaces</a>



<a href="https://msdn.microsoft.com/42efbd5b-6455-4319-a76e-cdb666fc36b8">Disk Quotas</a>



<a href="https://msdn.microsoft.com/fc9add5a-c9ef-462d-8125-128d48018717">IDiskQuotaControl</a>
 

 

