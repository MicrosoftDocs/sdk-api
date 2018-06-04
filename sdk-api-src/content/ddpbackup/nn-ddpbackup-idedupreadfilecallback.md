---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IDedupReadFileCallback interface


## -description


A callback interface, implemented by backup applications, that enables Data Deduplication to read content from metadata and container files residing in a backup store and optionally improve restore efficiency.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDedupReadFileCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDedupReadFileCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDedupReadFileCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25871056-5833-40DA-9C5B-690DCAB16E5C">OrderContainersRestore</a>
</td>
<td align="left" width="63%">
This method provides the application with the ability to influence the order of the pending reads that 
    are required to retrieve the target file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A3AFB530-ED97-4BEC-BF9D-668115E36A36">PreviewContainerRead</a>
</td>
<td align="left" width="63%">
Provides the application with a preview of the sequence of reads that are pending for a given container file extent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9A85B32B-7430-46AC-A9BF-2896651F40AF">ReadBackupFile</a>
</td>
<td align="left" width="63%">
 Reads data from a Data Deduplication store metadata or  container file located  in the backup store.

</td>
</tr>
</table> 


## -remarks



The <b>IDedupReadFileCallback</b> interface is implemented by a backup application and passed as a parameter to the <a href="dedup.idedupbackupsupport_restorefile">IDedupBackupSupport::RestoreFiles</a> method. The callback is used by Data Deduplication to read data from Data Duplication store containers in the backup store.  <b>IDedupReadFileCallback</b> also includes methods that applications can optionally implement to increase the efficiency of the Data Deduplication file restore process.




## -see-also




<a href="dedup.idedupbackupsupport_restorefile">IDedupBackupSupport::RestoreFiles</a>
 

 

