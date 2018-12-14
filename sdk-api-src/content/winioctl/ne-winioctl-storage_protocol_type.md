---
UID: NE:winioctl._STORAGE_PROTOCOL_TYPE
title: STORAGE_PROTOCOL_TYPE
author: windows-sdk-content
description: Specifies the protocol of a storage device.
old-location: fs\storage_protocol_type.htm
tech.root: fileio
ms.assetid: 8055B633-99EF-4AAE-AA80-FC09F357BEAB
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PSTORAGE_PROTOCOL_TYPE, PSTORAGE_PROTOCOL_TYPE, PSTORAGE_PROTOCOL_TYPE enumeration pointer [Files], ProtocolTypeAta, ProtocolTypeMaxReserved, ProtocolTypeNvme, ProtocolTypeProprietary, ProtocolTypeScsi, ProtocolTypeSd, ProtocolTypeUnknown, STORAGE_PROTOCOL_TYPE, _STORAGE_PROTOCOL_TYPE, _STORAGE_PROTOCOL_TYPE enumeration [Files], fs.storage_protocol_type, winioctl/PSTORAGE_PROTOCOL_TYPE, winioctl/ProtocolTypeAta, winioctl/ProtocolTypeMaxReserved, winioctl/ProtocolTypeNvme, winioctl/ProtocolTypeProprietary, winioctl/ProtocolTypeScsi, winioctl/ProtocolTypeSd, winioctl/ProtocolTypeUnknown, winioctl/_STORAGE_PROTOCOL_TYPE"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: winioctl.h
req.include-header: Windows.h
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
 - WinIoCtl.h
api_name:
 - STORAGE_PROTOCOL_TYPE
product: Windows
targetos: Windows
req.typenames: STORAGE_PROTOCOL_TYPE, *PSTORAGE_PROTOCOL_TYPE
req.redist: 
---

# STORAGE_PROTOCOL_TYPE enumeration


## -description


Specifies the protocol of a storage device.


## -enum-fields




### -field ProtocolTypeUnknown

Unknown protocol type.


### -field ProtocolTypeScsi

SCSI protocol type.


### -field ProtocolTypeAta

ATA protocol type.


### -field ProtocolTypeNvme

NVMe protocol type.


### -field ProtocolTypeSd

SD protocol type.


### -field ProtocolTypeUfs


### -field ProtocolTypeProprietary

 Vendor-specific protocol type.


### -field ProtocolTypeMaxReserved

Reserved.

