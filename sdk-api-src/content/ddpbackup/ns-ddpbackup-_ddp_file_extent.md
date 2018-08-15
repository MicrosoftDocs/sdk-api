---
UID: NS:ddpbackup._DDP_FILE_EXTENT
title: "_DDP_FILE_EXTENT"
author: windows-sdk-content
description: DDP_FILE_EXTENT represents the extent of data in a file that is to be read in a pending call to ReadBackupFile.
old-location: dedup\ddp_file_extent.htm
old-project: dedup
ms.assetid: B4AB7297-6FFE-4B93-ABDE-C15D7C90FA5B
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: DDP_FILE_EXTENT, DDP_FILE_EXTENT structure [Data Deduplication API], PDDP_FILE_EXTENT, PDDP_FILE_EXTENT structure pointer [Data Deduplication API], _DDP_FILE_EXTENT, ddpbackup/DDP_FILE_EXTENT, ddpbackup/PDDP_FILE_EXTENT, dedup.ddp_file_extent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ddpbackup.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: DDP_FILE_EXTENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DdpBackup.h
api_name:
 - DDP_FILE_EXTENT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DDP_FILE_EXTENT structure


## -description


<b>DDP_FILE_EXTENT</b> represents the extent of data in a 
     file that is to be read in a pending call to 
     <a href="https://msdn.microsoft.com/9A85B32B-7430-46AC-A9BF-2896651F40AF">ReadBackupFile</a>.


## -struct-fields




### -field Length

Length, in bytes, of the extent.


### -field Offset

Offset, in bytes, from the beginning of the file to the beginning of the extent.


## -remarks



Data Deduplication needs to read only the portions of a container file that back the restore target file.




## -see-also




<a href="https://msdn.microsoft.com/A3AFB530-ED97-4BEC-BF9D-668115E36A36">IDedupReadFileCallback::PreviewContainerRead</a>
 

 

