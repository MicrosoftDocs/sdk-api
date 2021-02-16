---
UID: NS:ddpbackup._DEDUP_CONTAINER_EXTENT
title: DEDUP_CONTAINER_EXTENT (ddpbackup.h)
description: A logical container file may be stored in a single segment or multiple segments in the backup store.
helpviewer_keywords: ["DEDUP_CONTAINER_EXTENT","DEDUP_CONTAINER_EXTENT structure [Data Deduplication API]","PDEDUP_CONTAINER_EXTENT","PDEDUP_CONTAINER_EXTENT structure pointer [Data Deduplication API]","ddpbackup/DEDUP_CONTAINER_EXTENT","ddpbackup/PDEDUP_CONTAINER_EXTENT","dedup.dedup_container_extent"]
old-location: dedup\dedup_container_extent.htm
tech.root: dedup
ms.assetid: D7CEC0C4-0472-467C-87F1-1496C9F08296
ms.date: 12/05/2018
ms.keywords: DEDUP_CONTAINER_EXTENT, DEDUP_CONTAINER_EXTENT structure [Data Deduplication API], PDEDUP_CONTAINER_EXTENT, PDEDUP_CONTAINER_EXTENT structure pointer [Data Deduplication API], ddpbackup/DEDUP_CONTAINER_EXTENT, ddpbackup/PDEDUP_CONTAINER_EXTENT, dedup.dedup_container_extent
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
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DEDUP_CONTAINER_EXTENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DEDUP_CONTAINER_EXTENT
 - ddpbackup/_DEDUP_CONTAINER_EXTENT
 - DEDUP_CONTAINER_EXTENT
 - ddpbackup/DEDUP_CONTAINER_EXTENT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DdpBackup.h
api_name:
 - DEDUP_CONTAINER_EXTENT
---

# DEDUP_CONTAINER_EXTENT structure


## -description

A logical container file may be stored in a single segment or multiple segments in the backup store. 
    <b>DEDUP_CONTAINER_EXTENT</b> represents a single 
    extent of a specific container file as stored in the backup store. The extent may be the full container file or a 
    portion of the file.

## -struct-fields

### -field ContainerIndex

The index in the container list passed to 
      <a href="/previous-versions/windows/desktop/api/ddpbackup/nf-ddpbackup-idedupreadfilecallback-ordercontainersrestore">IDedupReadFileCallback::OrderContainersRestore</a> 
      to which this container extent structure corresponds.

### -field StartOffset

Offset, in bytes, from the beginning of the container to the beginning of the extent.

### -field Length

Length, in bytes, of the extent.

## -remarks

For example, in an incremental backup scheme, the container may reside in the store either as one complete file 
     generated in a full backup, or as multiple incremental files that contain changes in the file since the previous 
     backup.

## -see-also

<a href="/previous-versions/windows/desktop/api/ddpbackup/nf-ddpbackup-idedupreadfilecallback-ordercontainersrestore">IDedupReadFileCallback::OrderContainersRestore</a>