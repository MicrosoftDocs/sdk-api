---
UID: NF:ddpbackup.IDedupReadFileCallback.OrderContainersRestore
title: IDedupReadFileCallback::OrderContainersRestore (ddpbackup.h)
description: This method provides the application with the ability to influence the order of the pending reads that are required to retrieve the target file.
helpviewer_keywords: ["IDedupReadFileCallback interface [Data Deduplication API]","OrderContainersRestore method","IDedupReadFileCallback.OrderContainersRestore","IDedupReadFileCallback::OrderContainersRestore","OrderContainersRestore","OrderContainersRestore method [Data Deduplication API]","OrderContainersRestore method [Data Deduplication API]","IDedupReadFileCallback interface","ddpbackup/IDedupReadFileCallback::OrderContainersRestore","dedup.idedupreadfilecallback_ordercontainersrestore"]
old-location: dedup\idedupreadfilecallback_ordercontainersrestore.htm
tech.root: dedup
ms.assetid: 25871056-5833-40DA-9C5B-690DCAB16E5C
ms.date: 12/05/2018
ms.keywords: IDedupReadFileCallback interface [Data Deduplication API],OrderContainersRestore method, IDedupReadFileCallback.OrderContainersRestore, IDedupReadFileCallback::OrderContainersRestore, OrderContainersRestore, OrderContainersRestore method [Data Deduplication API], OrderContainersRestore method [Data Deduplication API],IDedupReadFileCallback interface, ddpbackup/IDedupReadFileCallback::OrderContainersRestore, dedup.idedupreadfilecallback_ordercontainersrestore
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
 - IDedupReadFileCallback::OrderContainersRestore
 - ddpbackup/IDedupReadFileCallback::OrderContainersRestore
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
 - IDedupReadFileCallback.OrderContainersRestore
---

# IDedupReadFileCallback::OrderContainersRestore


## -description

This method provides the application with the ability to influence the order of the pending reads that 
    are required to retrieve the target file.

Given a list of container files that hold data for the 
    restore target file, generates a list of container file extents in a sorted order that results in an efficient 
    cross-container read plan from the backup store.

Implementation of this method by the application is 
    optional.

## -parameters

### -param NumberOfContainers [in]

Number of container paths in the <i>ContainerPaths</i> array.

### -param ContainerPaths [in]

Array of paths to container files that must be read in order to restore the file specified in the 
      <a href="/previous-versions/windows/desktop/api/ddpbackup/nf-ddpbackup-idedupbackupsupport-restorefiles">IDedupBackupSupport::RestoreFiles</a> 
      call. Each element is a full path from the root directory of the volume to a container file.

### -param ReadPlanEntries [out]

Pointer to a ULONG variable that receives the number of 
      <a href="/windows/desktop/api/ddpbackup/ns-ddpbackup-dedup_container_extent">DEDUP_CONTAINER_EXTENT</a> structures in the array 
      that the <i>ReadPlan</i> parameter points to.

### -param ReadPlan [out]

Pointer to a buffer that receives an array of 
      <a href="/windows/desktop/api/ddpbackup/ns-ddpbackup-dedup_container_extent">DEDUP_CONTAINER_EXTENT</a> structures.

## -returns

This method can return standard <b>HRESULT</b> values, such as 
      <b>S_OK</b>. It can also return converted 
      <a href="/windows/desktop/Debug/system-error-codes">system error codes</a> using the 
      <a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Possible return values 
      include the following.

## -remarks

Given a list of container files that hold data for the restore target file, the application optionally 
    generates a list of container store file extents in a sorted order that results in an efficient cross-container 
    read plan. For a backup store located on tape, this would normally be in tape order.

In the case where a container is stored in multiple extents in the backup store—for 
    example, as a result of an incremental backup sequence—the application may also return 
    multiple container extents for each logical container file.

The application may return 
    <b>S_OK</b> and <b>NULL</b> output parameters to skip the read plan 
    optimizations. In this case, container read order will be chosen by Data Deduplication.

## -see-also

<a href="/windows/desktop/api/ddpbackup/ns-ddpbackup-dedup_container_extent">DEDUP_CONTAINER_EXTENT</a>



<a href="/previous-versions/windows/desktop/api/ddpbackup/nn-ddpbackup-idedupreadfilecallback">IDedupReadFileCallback</a>