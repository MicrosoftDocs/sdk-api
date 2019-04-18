---
UID: NN:ddpbackup.IDedupBackupSupport
title: IDedupBackupSupport (ddpbackup.h)
author: windows-sdk-content
description: Provides a method for restoring a file from a backup store containing copies of Data Deduplication reparse points, metadata, and container files.
old-location: dedup\idedupbackupsupport.htm
tech.root: dedup
ms.assetid: 45AACC37-3C83-4DBA-8C18-26D76ED831BB
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDedupBackupSupport, IDedupBackupSupport interface [Data Deduplication API], IDedupBackupSupport interface [Data Deduplication API],described, ddpbackup/IDedupBackupSupport, dedup.idedupbackupsupport
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
req.idl: DdpBackup.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: DdpBackup.dll
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DdpBackup.dll
api_name:
 - IDedupBackupSupport
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDedupBackupSupport interface


## -description


Provides a method for restoring a file from a backup store containing copies of Data Deduplication 
     reparse points, metadata, and container files.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDedupBackupSupport</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDedupBackupSupport</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDedupBackupSupport</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CFBB0B59-2869-4A30-8F2F-A473372B1E68">RestoreFiles</a>
</td>
<td align="left" width="63%">
Reconstructs a set of files from a backup store that contains the fully optimized version of the files 
     (reparse points) and the Data Deduplication store.

</td>
</tr>
</table> 


## -remarks



 A backup application uses the 
     <b>IDedupBackupSupport</b> interface to drive the restore 
     process for a select file from a backup store that contains the fully optimized version of the file (reparse 
     point) and the Data Deduplication store.

This interface is not useful when the backup store contains a copy of the original, non-optimized file.

Applications that use the <b>IDedupBackupSupport</b> 
     interface must also implement the 
     <a href="https://msdn.microsoft.com/0B7F5A5B-EB60-4BAF-86AF-D9101F3B482C">IDedupReadFileCallback</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/0B7F5A5B-EB60-4BAF-86AF-D9101F3B482C">IDedupReadFileCallback</a>
 

 

