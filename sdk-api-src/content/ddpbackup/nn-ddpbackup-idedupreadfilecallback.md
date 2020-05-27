---
UID: NN:ddpbackup.IDedupReadFileCallback
title: IDedupReadFileCallback (ddpbackup.h)
description: A callback interface, implemented by backup applications, that enables Data Deduplication to read content from metadata and container files residing in a backup store and optionally improve restore efficiency.
helpviewer_keywords: ["IDedupReadFileCallback","IDedupReadFileCallback interface [Data Deduplication API]","IDedupReadFileCallback interface [Data Deduplication API]","described","ddpbackup/IDedupReadFileCallback","dedup.idedupreadfilecallback"]
old-location: dedup\idedupreadfilecallback.htm
tech.root: dedup
ms.assetid: 0B7F5A5B-EB60-4BAF-86AF-D9101F3B482C
ms.date: 12/05/2018
ms.keywords: IDedupReadFileCallback, IDedupReadFileCallback interface [Data Deduplication API], IDedupReadFileCallback interface [Data Deduplication API],described, ddpbackup/IDedupReadFileCallback, dedup.idedupreadfilecallback
f1_keywords:
- ddpbackup/IDedupReadFileCallback
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDedupReadFileCallback interface


## -description


A callback interface, implemented by backup applications, that enables Data Deduplication to read content from metadata and container files residing in a backup store and optionally improve restore efficiency.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDedupReadFileCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDedupReadFileCallback</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/ddpbackup/nf-ddpbackup-idedupreadfilecallback-ordercontainersrestore">OrderContainersRestore</a>
</td>
<td align="left" width="63%">
This method provides the application with the ability to influence the order of the pending reads that 
    are required to retrieve the target file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/ddpbackup/nf-ddpbackup-idedupreadfilecallback-previewcontainerread">PreviewContainerRead</a>
</td>
<td align="left" width="63%">
Provides the application with a preview of the sequence of reads that are pending for a given container file extent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/ddpbackup/nf-ddpbackup-idedupreadfilecallback-readbackupfile">ReadBackupFile</a>
</td>
<td align="left" width="63%">
 Reads data from a Data Deduplication store metadata or  container file located  in the backup store.

</td>
</tr>
</table> 


## -remarks



The <b>IDedupReadFileCallback</b> interface is implemented by a backup application and passed as a parameter to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/ddpbackup/nf-ddpbackup-idedupbackupsupport-restorefiles">IDedupBackupSupport::RestoreFiles</a> method. The callback is used by Data Deduplication to read data from Data Duplication store containers in the backup store.  <b>IDedupReadFileCallback</b> also includes methods that applications can optionally implement to increase the efficiency of the Data Deduplication file restore process.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/ddpbackup/nf-ddpbackup-idedupbackupsupport-restorefiles">IDedupBackupSupport::RestoreFiles</a>
 

 

