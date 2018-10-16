---
UID: NF:dskquota.IDiskQuotaUserBatch.FlushToDisk
title: IDiskQuotaUserBatch::FlushToDisk
author: windows-sdk-content
description: Writes user object changes to disk in a single call to the underlying file system.
old-location: fs\idiskquotauserbatch_flushtodisk.htm
tech.root: fileio
ms.assetid: 2d147224-64d8-4c15-b860-e6dd216cb170
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: FlushToDisk, FlushToDisk method [Files], FlushToDisk method [Files],IDiskQuotaUserBatch interface, IDiskQuotaUserBatch interface [Files],FlushToDisk method, IDiskQuotaUserBatch.FlushToDisk, IDiskQuotaUserBatch::FlushToDisk, _win32_idiskquotauserbatch_flushtodisk, base.idiskquotauserbatch_flushtodisk, dskquota/IDiskQuotaUserBatch::FlushToDisk, fs.idiskquotauserbatch_flushtodisk
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
 - IDiskQuotaUserBatch.FlushToDisk
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiskQuotaUserBatch::FlushToDisk


## -description


Writes user object changes to disk in a single call to the underlying file system.


## -parameters






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



There are limitations on the amount of information that can be written to disk in a single call to the file system. The flush operation may generate multiple calls to the file system. Nonetheless, the batch operation will be more efficient than a single call for each user object.




## -see-also




<a href="https://msdn.microsoft.com/c1f79e2e-834b-41dc-a15f-6dd1034d021b">Disk Management Interfaces</a>



<a href="https://msdn.microsoft.com/42efbd5b-6455-4319-a76e-cdb666fc36b8">Disk Quotas</a>



<a href="https://msdn.microsoft.com/6cb3da5d-8e4c-45de-b9cf-0f6abf3f1932">IDiskQuotaUserBatch</a>
 

 

