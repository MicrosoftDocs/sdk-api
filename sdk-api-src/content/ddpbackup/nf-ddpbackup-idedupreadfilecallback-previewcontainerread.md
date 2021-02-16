---
UID: NF:ddpbackup.IDedupReadFileCallback.PreviewContainerRead
title: IDedupReadFileCallback::PreviewContainerRead (ddpbackup.h)
description: Provides the application with a preview of the sequence of reads that are pending for a given container file extent.
helpviewer_keywords: ["IDedupReadFileCallback interface [Data Deduplication API]","PreviewContainerRead method","IDedupReadFileCallback.PreviewContainerRead","IDedupReadFileCallback::PreviewContainerRead","PreviewContainerRead","PreviewContainerRead method [Data Deduplication API]","PreviewContainerRead method [Data Deduplication API]","IDedupReadFileCallback interface","ddpbackup/IDedupReadFileCallback::PreviewContainerRead","dedup.idedupreadfilecallback_previewcontainerread"]
old-location: dedup\idedupreadfilecallback_previewcontainerread.htm
tech.root: dedup
ms.assetid: A3AFB530-ED97-4BEC-BF9D-668115E36A36
ms.date: 12/05/2018
ms.keywords: IDedupReadFileCallback interface [Data Deduplication API],PreviewContainerRead method, IDedupReadFileCallback.PreviewContainerRead, IDedupReadFileCallback::PreviewContainerRead, PreviewContainerRead, PreviewContainerRead method [Data Deduplication API], PreviewContainerRead method [Data Deduplication API],IDedupReadFileCallback interface, ddpbackup/IDedupReadFileCallback::PreviewContainerRead, dedup.idedupreadfilecallback_previewcontainerread
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
 - IDedupReadFileCallback::PreviewContainerRead
 - ddpbackup/IDedupReadFileCallback::PreviewContainerRead
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
 - IDedupReadFileCallback.PreviewContainerRead
---

# IDedupReadFileCallback::PreviewContainerRead


## -description

Provides the application with a preview of the sequence of reads that are pending for a given container file extent.

## -parameters

### -param FileFullPath [in]

The full path from the root directory of the volume to the container file.

### -param NumberOfReads [in]

Number of <a href="/windows/desktop/api/ddpbackup/ns-ddpbackup-ddp_file_extent">DDP_FILE_EXTENT</a> structures in the array that the <i>ReadOffsets</i> parameter points to.

### -param ReadOffsets [in]

Pointer to an array of <a href="/windows/desktop/api/ddpbackup/ns-ddpbackup-ddp_file_extent">DDP_FILE_EXTENT</a> structures.

## -returns

This method can return standard <b>HRESULT</b> values, such as <b>S_OK</b>. It can also return converted <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Possible return values include the following.

## -remarks

<b>PreviewContainerRead</b> is called for each container file extent reported by <a href="/previous-versions/windows/desktop/api/ddpbackup/nf-ddpbackup-idedupreadfilecallback-ordercontainersrestore">IDedupReadFileCallback::OrderContainersRestore</a>. The application may use this preview as a per-container extent read plan to increase the efficiency of the pending reads. For example, the application may choose to perform read-ahead to improve throughput or to cache read buffers to improve overall performance across parallel file restore operations.

## -see-also

<a href="/windows/desktop/api/ddpbackup/ns-ddpbackup-ddp_file_extent">DDP_FILE_EXTENT</a>



<a href="/previous-versions/windows/desktop/api/ddpbackup/nn-ddpbackup-idedupreadfilecallback">IDedupReadFileCallback</a>