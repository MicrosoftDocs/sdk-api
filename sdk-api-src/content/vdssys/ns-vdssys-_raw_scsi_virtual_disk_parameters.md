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

# _RAW_SCSI_VIRTUAL_DISK_PARAMETERS structure


## -description


Contains raw SCSI virtual disk request parameters.


## -struct-fields




### -field Version

A <a href="https://msdn.microsoft.com/EE0567C8-D479-436B-B1AC-7D1C4AC3B403">RAW_SCSI_VIRTUAL_DISK_VERSION</a> enumeration that specifies the version of the <b>RAW_SCSI_VIRTUAL_DISK_PARAMETERS</b> structure being passed to or from the VHD functions. 



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

