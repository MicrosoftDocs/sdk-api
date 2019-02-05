---
UID: NF:dskquota.IDiskQuotaUserBatch.Remove
title: IDiskQuotaUserBatch::Remove
author: windows-sdk-content
description: Removes an IDiskQuotaUser pointer from the batch list.
old-location: fs\idiskquotauserbatch_remove.htm
tech.root: FileIO
ms.assetid: 102e9a07-9958-4d47-acd3-6b81e83a5ea7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDiskQuotaUserBatch interface [Files],Remove method, IDiskQuotaUserBatch.Remove, IDiskQuotaUserBatch::Remove, Remove, Remove method [Files], Remove method [Files],IDiskQuotaUserBatch interface, _win32_idiskquotauserbatch_remove, base.idiskquotauserbatch_remove, dskquota/IDiskQuotaUserBatch::Remove, fs.idiskquotauserbatch_remove
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
 - IDiskQuotaUserBatch.Remove
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiskQuotaUserBatch::Remove


## -description


Removes an 
<a href="https://msdn.microsoft.com/27edbebc-35b4-4f6a-87cc-d8a99782f405">IDiskQuotaUser</a> pointer from the batch list.


## -parameters




### -param pUser [in]

A pointer to the quota user object's 
<a href="https://msdn.microsoft.com/27edbebc-35b4-4f6a-87cc-d8a99782f405">IDiskQuotaUser</a> interface.


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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Quota user object not found in batch.

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



<a href="https://msdn.microsoft.com/6cb3da5d-8e4c-45de-b9cf-0f6abf3f1932">IDiskQuotaUserBatch</a>
 

 

