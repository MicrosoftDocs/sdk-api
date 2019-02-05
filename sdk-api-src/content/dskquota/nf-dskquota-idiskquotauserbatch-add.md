---
UID: NF:dskquota.IDiskQuotaUserBatch.Add
title: IDiskQuotaUserBatch::Add
author: windows-sdk-content
description: Adds an IDiskQuotaUser pointer to the batch list.
old-location: fs\idiskquotauserbatch_add.htm
tech.root: FileIO
ms.assetid: 8b0876d2-55ba-4eaa-b317-8ea1d2f5ff4f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Add, Add method [Files], Add method [Files],IDiskQuotaUserBatch interface, IDiskQuotaUserBatch interface [Files],Add method, IDiskQuotaUserBatch.Add, IDiskQuotaUserBatch::Add, _win32_idiskquotauserbatch_add, base.idiskquotauserbatch_add, dskquota/IDiskQuotaUserBatch::Add, fs.idiskquotauserbatch_add
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
 - IDiskQuotaUserBatch.Add
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiskQuotaUserBatch::Add


## -description


Adds an 
<a href="https://msdn.microsoft.com/27edbebc-35b4-4f6a-87cc-d8a99782f405">IDiskQuotaUser</a> pointer to the batch list. This method calls <b>AddRef</b> on the <i>pUser</i> interface pointer. <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">Release</a> is automatically called on each contained 
<a href="https://msdn.microsoft.com/27edbebc-35b4-4f6a-87cc-d8a99782f405">IDiskQuotaUser</a> interface pointer when the batch object is destroyed.

When setting values on a quota user object in preparation for batch processing, specify <b>FALSE</b> for the <i>fWriteThrough</i> parameter in the 
<a href="https://msdn.microsoft.com/f7c99415-685b-4a21-ac7b-68f4816aafb0">IDiskQuotaUser::SetQuotaLimit</a> and 
<a href="https://msdn.microsoft.com/7c641a1c-fb04-4039-92bd-d3a1c7045355">IDiskQuotaUser::SetQuotaThreshold</a> methods. This stores the values in memory without writing to disk. To write the changes to disk, call the 
<a href="https://msdn.microsoft.com/2d147224-64d8-4c15-b860-e6dd216cb170">IDiskQuotaUserBatch::FlushToDisk</a> method.


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
 

 

