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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDedupReadFileCallback
 - ddpbackup/IDedupReadFileCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DdpBackup.h
api_name:
 - IDedupReadFileCallback
---

# IDedupReadFileCallback interface


## -description

A callback interface, implemented by backup applications, that enables Data Deduplication to read content from metadata and container files residing in a backup store and optionally improve restore efficiency.

## -inheritance

The <b>IDedupReadFileCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDedupReadFileCallback</b> also has these types of members:

## -remarks

The <b>IDedupReadFileCallback</b> interface is implemented by a backup application and passed as a parameter to the <a href="/previous-versions/windows/desktop/api/ddpbackup/nf-ddpbackup-idedupbackupsupport-restorefiles">IDedupBackupSupport::RestoreFiles</a> method. The callback is used by Data Deduplication to read data from Data Duplication store containers in the backup store.  <b>IDedupReadFileCallback</b> also includes methods that applications can optionally implement to increase the efficiency of the Data Deduplication file restore process.

## -see-also

<a href="/previous-versions/windows/desktop/api/ddpbackup/nf-ddpbackup-idedupbackupsupport-restorefiles">IDedupBackupSupport::RestoreFiles</a>
