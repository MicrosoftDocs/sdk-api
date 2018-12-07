---
UID: NN:dskquota.IDiskQuotaUserBatch
title: IDiskQuotaUserBatch
author: windows-sdk-content
description: Adds multiple quota user objects to a container that is then submitted for update in a single call.
old-location: fs\idiskquotauserbatch.htm
tech.root: fileio
ms.assetid: 6cb3da5d-8e4c-45de-b9cf-0f6abf3f1932
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDiskQuotaUserBatch, IDiskQuotaUserBatch interface [Files], IDiskQuotaUserBatch interface [Files],described, _win32_idiskquotauserbatch, base.idiskquotauserbatch, dskquota/IDiskQuotaUserBatch, fs.idiskquotauserbatch
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
 - IDiskQuotaUserBatch
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiskQuotaUserBatch interface


## -description


Adds multiple quota user objects to a container that is then submitted for update in a single call. This reduces the number of calls to the underlying file system, improving update efficiency when a large number of user objects must be updated. This interface is instantiated by using the 
<a href="https://msdn.microsoft.com/c1c5a71f-4a2f-4bf9-b28f-11b87a558771">IDiskQuotaControl::CreateUserBatch</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDiskQuotaUserBatch</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDiskQuotaUserBatch</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDiskQuotaUserBatch</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b0876d2-55ba-4eaa-b317-8ea1d2f5ff4f">Add</a>
</td>
<td align="left" width="63%">
Adds an <a href="https://msdn.microsoft.com/27edbebc-35b4-4f6a-87cc-d8a99782f405">IDiskQuotaUser</a> pointer to the batch list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2d147224-64d8-4c15-b860-e6dd216cb170">FlushToDisk</a>
</td>
<td align="left" width="63%">
Writes user object changes to disk in a single call to the underlying file system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/102e9a07-9958-4d47-acd3-6b81e83a5ea7">Remove</a>
</td>
<td align="left" width="63%">
Removes an <a href="https://msdn.microsoft.com/27edbebc-35b4-4f6a-87cc-d8a99782f405">IDiskQuotaUser</a> pointer from the batch list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f3c791a9-4976-4e04-903f-a1afffd01f7c">RemoveAll</a>
</td>
<td align="left" width="63%">
Removes all <a href="https://msdn.microsoft.com/27edbebc-35b4-4f6a-87cc-d8a99782f405">IDiskQuotaUser</a> pointers from the batch list.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/c1f79e2e-834b-41dc-a15f-6dd1034d021b">Disk Management Interfaces</a>



<a href="https://msdn.microsoft.com/42efbd5b-6455-4319-a76e-cdb666fc36b8">Disk Quotas</a>
 

 

