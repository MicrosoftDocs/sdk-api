---
UID: NF:ddpbackup.IDedupReadFileCallback.PreviewContainerRead
title: IDedupReadFileCallback::PreviewContainerRead
author: windows-sdk-content
description: Provides the application with a preview of the sequence of reads that are pending for a given container file extent.
old-location: dedup\idedupreadfilecallback_previewcontainerread.htm
tech.root: dedup
ms.assetid: A3AFB530-ED97-4BEC-BF9D-668115E36A36
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDedupReadFileCallback interface [Data Deduplication API],PreviewContainerRead method, IDedupReadFileCallback.PreviewContainerRead, IDedupReadFileCallback::PreviewContainerRead, PreviewContainerRead, PreviewContainerRead method [Data Deduplication API], PreviewContainerRead method [Data Deduplication API],IDedupReadFileCallback interface, ddpbackup/IDedupReadFileCallback::PreviewContainerRead, dedup.idedupreadfilecallback_previewcontainerread
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IDedupReadFileCallback.PreviewContainerRead
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDedupReadFileCallback::PreviewContainerRead


## -description


Provides the application with a preview of the sequence of reads that are pending for a given container file extent.


## -parameters




### -param FileFullPath [in]

The full path from the root directory of the volume to the container file.


### -param NumberOfReads [in]

Number of <a href="https://msdn.microsoft.com/B4AB7297-6FFE-4B93-ABDE-C15D7C90FA5B">DDP_FILE_EXTENT</a> structures in the array that the <i>ReadOffsets</i> parameter points to.


### -param ReadOffsets [in]

Pointer to an array of <a href="https://msdn.microsoft.com/B4AB7297-6FFE-4B93-ABDE-C15D7C90FA5B">DDP_FILE_EXTENT</a> structures.


## -returns



This method can return standard <b>HRESULT</b> values, such as <b>S_OK</b>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="_com_hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Possible return values include the following.




## -remarks



<b>PreviewContainerRead</b> is called for each container file extent reported by <a href="https://msdn.microsoft.com/25871056-5833-40DA-9C5B-690DCAB16E5C">IDedupReadFileCallback::OrderContainersRestore</a>. The application may use this preview as a per-container extent read plan to increase the efficiency of the pending reads. For example, the application may choose to perform read-ahead to improve throughput or to cache read buffers to improve overall performance across parallel file restore operations.




## -see-also




<a href="https://msdn.microsoft.com/B4AB7297-6FFE-4B93-ABDE-C15D7C90FA5B">DDP_FILE_EXTENT</a>



<a href="https://msdn.microsoft.com/0B7F5A5B-EB60-4BAF-86AF-D9101F3B482C">IDedupReadFileCallback</a>
 

 

