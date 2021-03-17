---
UID: NS:virtdisk._RAW_SCSI_VIRTUAL_DISK_PARAMETERS
title: RAW_SCSI_VIRTUAL_DISK_PARAMETERS (virtdisk.h)
description: Contains raw SCSI virtual disk request parameters.
helpviewer_keywords: ["*PRAW_SCSI_VIRTUAL_DISK_PARAMETERS","PRAW_SCSI_VIRTUAL_DISK_PARAMETERS","PRAW_SCSI_VIRTUAL_DISK_PARAMETERS structure pointer [VHD]","RAW_SCSI_VIRTUAL_DISK_PARAMETERS","RAW_SCSI_VIRTUAL_DISK_PARAMETERS structure [VHD]","_RAW_SCSI_VIRTUAL_DISK_PARAMETERS","vdssys/PRAW_SCSI_VIRTUAL_DISK_PARAMETERS","vdssys/RAW_SCSI_VIRTUAL_DISK_PARAMETERS","vhd.raw_scsi_virtual_disk_parameters","virtdisk/PRAW_SCSI_VIRTUAL_DISK_PARAMETERS","virtdisk/RAW_SCSI_VIRTUAL_DISK_PARAMETERS"]
old-location: vhd\raw_scsi_virtual_disk_parameters.htm
tech.root: VStor
ms.assetid: E6E6BD59-F7BC-4523-B368-6EBE12285593
ms.date: 12/05/2018
ms.keywords: '*PRAW_SCSI_VIRTUAL_DISK_PARAMETERS, PRAW_SCSI_VIRTUAL_DISK_PARAMETERS, PRAW_SCSI_VIRTUAL_DISK_PARAMETERS structure pointer [VHD], RAW_SCSI_VIRTUAL_DISK_PARAMETERS, RAW_SCSI_VIRTUAL_DISK_PARAMETERS structure [VHD], _RAW_SCSI_VIRTUAL_DISK_PARAMETERS, vdssys/PRAW_SCSI_VIRTUAL_DISK_PARAMETERS, vdssys/RAW_SCSI_VIRTUAL_DISK_PARAMETERS, vhd.raw_scsi_virtual_disk_parameters, virtdisk/PRAW_SCSI_VIRTUAL_DISK_PARAMETERS, virtdisk/RAW_SCSI_VIRTUAL_DISK_PARAMETERS'
req.header: virtdisk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: RAW_SCSI_VIRTUAL_DISK_PARAMETERS, *PRAW_SCSI_VIRTUAL_DISK_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RAW_SCSI_VIRTUAL_DISK_PARAMETERS
 - virtdisk/_RAW_SCSI_VIRTUAL_DISK_PARAMETERS
 - PRAW_SCSI_VIRTUAL_DISK_PARAMETERS
 - virtdisk/PRAW_SCSI_VIRTUAL_DISK_PARAMETERS
 - RAW_SCSI_VIRTUAL_DISK_PARAMETERS
 - virtdisk/RAW_SCSI_VIRTUAL_DISK_PARAMETERS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VirtDisk.h
 - vdssys.h
api_name:
 - RAW_SCSI_VIRTUAL_DISK_PARAMETERS
---

# RAW_SCSI_VIRTUAL_DISK_PARAMETERS structure


## -description

Contains raw SCSI virtual disk request parameters.

## -struct-fields

### -field Version

A <a href="/windows/win32/api/virtdisk/ne-virtdisk-raw_scsi_virtual_disk_version">RAW_SCSI_VIRTUAL_DISK_VERSION</a> enumeration that specifies the version of the <b>RAW_SCSI_VIRTUAL_DISK_PARAMETERS</b> structure being passed to or from the VHD functions.

### -field Version1

A structure with the following members.

### -field Version1.RSVDHandle

If TRUE, indicates the operation will be transported to the virtual disk using the RSVD protocol.

### -field Version1.DataIn

If TRUE, indicates the SCSI command will read data from the DataBuffer. If FALSE, indicates data may be written.

### -field Version1.CdbLength

Length, in bytes, of the command descriptor block (CDB) contained in the CDB member.

### -field Version1.SenseInfoLength

Length, in bytes, of the sense buffer.

### -field Version1.SrbFlags

Caller-supplied SRB_FLAGS-prefixed bit flag specifying the requested operation. Flags are defined in srb.h.

### -field Version1.DataTransferLength

Length, in bytes, of the buffer to be transferred.

### -field Version1.DataBuffer

A pointer to the SCSI data buffer.

### -field Version1.SenseInfo

A pointer to a buffer to receive SCSI sense info after completion of the command.

### -field Version1.Cdb

Caller-supplied CDB data. (The CDB structure is declared in scsi.h.)

