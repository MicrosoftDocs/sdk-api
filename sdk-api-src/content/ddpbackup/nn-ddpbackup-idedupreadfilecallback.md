---
UID: NN:ddpbackup.IDedupReadFileCallback
title: IDedupReadFileCallback
author: windows-sdk-content
description: A callback interface, implemented by backup applications, that enables Data Deduplication to read content from metadata and container files residing in a backup store and optionally improve restore efficiency.
old-location: dedup\idedupreadfilecallback.htm
tech.root: dedup
ms.assetid: 0B7F5A5B-EB60-4BAF-86AF-D9101F3B482C
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IDedupReadFileCallback, IDedupReadFileCallback interface [Data Deduplication API], IDedupReadFileCallback interface [Data Deduplication API],described, ddpbackup/IDedupReadFileCallback, dedup.idedupreadfilecallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: ddpbackup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DdpBackup.h
api_name:
 - IDedupReadFileCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

