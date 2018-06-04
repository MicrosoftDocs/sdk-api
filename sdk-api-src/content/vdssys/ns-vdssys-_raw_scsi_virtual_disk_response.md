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

# _RAW_SCSI_VIRTUAL_DISK_RESPONSE structure


## -description


Contains raw SCSI virtual disk response parameters.


## -struct-fields




### -field Version

A <a href="https://msdn.microsoft.com/EE0567C8-D479-436B-B1AC-7D1C4AC3B403">RAW_SCSI_VIRTUAL_DISK_VERSION</a> enumeration that specifies the version of the <a href="https://msdn.microsoft.com/E6E6BD59-F7BC-4523-B368-6EBE12285593">RAW_SCSI_VIRTUAL_DISK_PARAMETERS</a> structure being passed to or from the VHD functions. 



### -field Version1

A structure with the following member.


### -field Version1.ScsiStatus

A SRB_STATUS-prefixed status value (defined in srb.h).


### -field Version1.SenseInfoLength

Length, in bytes, of the sense buffer.


### -field Version1.DataTransferLength

Length, in bytes, of the buffer to be transferred. 


