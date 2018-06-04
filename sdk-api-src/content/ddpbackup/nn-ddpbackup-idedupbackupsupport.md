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
 

 

