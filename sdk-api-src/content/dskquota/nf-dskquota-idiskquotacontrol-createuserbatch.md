---
UID: NF:dskquota.IDiskQuotaControl.CreateUserBatch
title: IDiskQuotaControl::CreateUserBatch
author: windows-sdk-content
description: Creates a batching object for optimizing updates to the quota settings of multiple users simultaneously.
old-location: fs\idiskquotacontrol_createuserbatch.htm
tech.root: fileio
ms.assetid: c1c5a71f-4a2f-4bf9-b28f-11b87a558771
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateUserBatch, CreateUserBatch method [Files], CreateUserBatch method [Files],IDiskQuotaControl interface, IDiskQuotaControl interface [Files],CreateUserBatch method, IDiskQuotaControl.CreateUserBatch, IDiskQuotaControl::CreateUserBatch, _win32_idiskquotacontrol_createuserbatch, base.idiskquotacontrol_createuserbatch, dskquota/IDiskQuotaControl::CreateUserBatch, fs.idiskquotacontrol_createuserbatch
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
 - IDiskQuotaControl.CreateUserBatch
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiskQuotaControl::CreateUserBatch


## -description


Creates a batching object for optimizing updates to the quota settings of multiple users simultaneously.


## -parameters




### -param ppBatch [out]

A pointer to the 
<a href="https://msdn.microsoft.com/6cb3da5d-8e4c-45de-b9cf-0f6abf3f1932">IDiskQuotaUserBatch</a> interface pointer.


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
The <i>ppBatch</i> parameter is <b>NULL</b>.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected exception occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c1f79e2e-834b-41dc-a15f-6dd1034d021b">Disk Management Interfaces</a>



<a href="https://msdn.microsoft.com/42efbd5b-6455-4319-a76e-cdb666fc36b8">Disk Quotas</a>



<a href="https://msdn.microsoft.com/fc9add5a-c9ef-462d-8125-128d48018717">IDiskQuotaControl</a>
 

 

