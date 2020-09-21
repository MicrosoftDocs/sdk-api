---
UID: NS:ddpbackup._DDP_FILE_EXTENT
title: DDP_FILE_EXTENT (ddpbackup.h)
description: DDP_FILE_EXTENT represents the extent of data in a file that is to be read in a pending call to ReadBackupFile.
helpviewer_keywords: ["DDP_FILE_EXTENT","DDP_FILE_EXTENT structure [Data Deduplication API]","PDDP_FILE_EXTENT","PDDP_FILE_EXTENT structure pointer [Data Deduplication API]","ddpbackup/DDP_FILE_EXTENT","ddpbackup/PDDP_FILE_EXTENT","dedup.ddp_file_extent"]
old-location: dedup\ddp_file_extent.htm
tech.root: dedup
ms.assetid: B4AB7297-6FFE-4B93-ABDE-C15D7C90FA5B
ms.date: 12/05/2018
ms.keywords: DDP_FILE_EXTENT, DDP_FILE_EXTENT structure [Data Deduplication API], PDDP_FILE_EXTENT, PDDP_FILE_EXTENT structure pointer [Data Deduplication API], ddpbackup/DDP_FILE_EXTENT, ddpbackup/PDDP_FILE_EXTENT, dedup.ddp_file_extent
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
req.typenames: DDP_FILE_EXTENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDP_FILE_EXTENT
 - ddpbackup/_DDP_FILE_EXTENT
 - DDP_FILE_EXTENT
 - ddpbackup/DDP_FILE_EXTENT
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
 - DDP_FILE_EXTENT
---

# DDP_FILE_EXTENT structure


## -description

<b>DDP_FILE_EXTENT</b> represents the extent of data in a 
     file that is to be read in a pending call to 
     <a href="/previous-versions/windows/desktop/api/ddpbackup/nf-ddpbackup-idedupreadfilecallback-readbackupfile">ReadBackupFile</a>.

## -struct-fields

### -field Length

Length, in bytes, of the extent.

### -field Offset

Offset, in bytes, from the beginning of the file to the beginning of the extent.

## -remarks

Data Deduplication needs to read only the portions of a container file that back the restore target file.

## -see-also

<a href="/previous-versions/windows/desktop/api/ddpbackup/nf-ddpbackup-idedupreadfilecallback-previewcontainerread">IDedupReadFileCallback::PreviewContainerRead</a>