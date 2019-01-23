---
UID: NS:virtdisk._RAW_SCSI_VIRTUAL_DISK_RESPONSE
title: RAW_SCSI_VIRTUAL_DISK_RESPONSE
author: windows-sdk-content
description: Contains raw SCSI virtual disk response parameters.
old-location: vhd\raw_scsi_virtual_disk_response.htm
tech.root: VStor
ms.assetid: CF3240A0-134B-4494-8451-7F8C6429D435
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PRAW_SCSI_VIRTUAL_DISK_RESPONSE, PRAW_SCSI_VIRTUAL_DISK_RESPONSE, PRAW_SCSI_VIRTUAL_DISK_RESPONSE structure pointer [VHD], RAW_SCSI_VIRTUAL_DISK_RESPONSE, RAW_SCSI_VIRTUAL_DISK_RESPONSE structure [VHD], _RAW_SCSI_VIRTUAL_DISK_RESPONSE, vdssys/PRAW_SCSI_VIRTUAL_DISK_RESPONSE, vdssys/RAW_SCSI_VIRTUAL_DISK_RESPONSE, vhd.raw_scsi_virtual_disk_response, virtdisk/PRAW_SCSI_VIRTUAL_DISK_RESPONSE, virtdisk/RAW_SCSI_VIRTUAL_DISK_RESPONSE"
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VirtDisk.h
 - vdssys.h
api_name:
 - RAW_SCSI_VIRTUAL_DISK_RESPONSE
product: Windows
targetos: Windows
req.typenames: RAW_SCSI_VIRTUAL_DISK_RESPONSE, *PRAW_SCSI_VIRTUAL_DISK_RESPONSE
req.redist: 
---

# RAW_SCSI_VIRTUAL_DISK_RESPONSE structure


## -description


Contains raw SCSI virtual disk response parameters.


## -struct-fields




### -field Version

A <a href="https://msdn.microsoft.com/en-us/library/Mt764775(v=VS.85).aspx">RAW_SCSI_VIRTUAL_DISK_VERSION</a> enumeration that specifies the version of the <a href="https://msdn.microsoft.com/en-us/library/Mt764773(v=VS.85).aspx">RAW_SCSI_VIRTUAL_DISK_PARAMETERS</a> structure being passed to or from the VHD functions. 



### -field Version1

A structure with the following member.


### -field Version1.ScsiStatus

A SRB_STATUS-prefixed status value (defined in srb.h).


### -field Version1.SenseInfoLength

Length, in bytes, of the sense buffer.


### -field Version1.DataTransferLength

Length, in bytes, of the buffer to be transferred. 


