---
UID: NE:winioctl._STORAGE_BUS_TYPE
title: STORAGE_BUS_TYPE
description: Specifies the various types of storage buses.
helpviewer_keywords: ["*PSTORAGE_BUS_TYPE","BusType1394","BusTypeAta","BusTypeAtapi","BusTypeFibre","BusTypeMaxReserved","BusTypeRAID","BusTypeSas","BusTypeSata","BusTypeScsi","BusTypeSsa","BusTypeUnknown","BusTypeUsb","BusTypeiSCSI","PSTORAGE_BUS_TYPE","PSTORAGE_BUS_TYPE enumeration pointer","STORAGE_BUS_TYPE","STORAGE_BUS_TYPE enumeration","_win32_storage_bus_type","base.storage_bus_type","winioctl/BusType1394","winioctl/BusTypeAta","winioctl/BusTypeAtapi","winioctl/BusTypeFibre","winioctl/BusTypeMaxReserved","winioctl/BusTypeRAID","winioctl/BusTypeSas","winioctl/BusTypeSata","winioctl/BusTypeScsi","winioctl/BusTypeSsa","winioctl/BusTypeUnknown","winioctl/BusTypeUsb","winioctl/BusTypeiSCSI","winioctl/PSTORAGE_BUS_TYPE","winioctl/STORAGE_BUS_TYPE"]
old-location: base\storage_bus_type.htm
tech.root: base
ms.assetid: fb5a17f7-8ddb-4738-83e1-f00abc3555d2
ms.date: 12/05/2018
ms.keywords: '*PSTORAGE_BUS_TYPE, BusType1394, BusTypeAta, BusTypeAtapi, BusTypeFibre, BusTypeMaxReserved, BusTypeRAID, BusTypeSas, BusTypeSata, BusTypeScsi, BusTypeSsa, BusTypeUnknown, BusTypeUsb, BusTypeiSCSI, PSTORAGE_BUS_TYPE, PSTORAGE_BUS_TYPE enumeration pointer, STORAGE_BUS_TYPE, STORAGE_BUS_TYPE enumeration, _win32_storage_bus_type, base.storage_bus_type, winioctl/BusType1394, winioctl/BusTypeAta, winioctl/BusTypeAtapi, winioctl/BusTypeFibre, winioctl/BusTypeMaxReserved, winioctl/BusTypeRAID, winioctl/BusTypeSas, winioctl/BusTypeSata, winioctl/BusTypeScsi, winioctl/BusTypeSsa, winioctl/BusTypeUnknown, winioctl/BusTypeUsb, winioctl/BusTypeiSCSI, winioctl/PSTORAGE_BUS_TYPE, winioctl/STORAGE_BUS_TYPE'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
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
req.typenames: STORAGE_BUS_TYPE, *PSTORAGE_BUS_TYPE
req.redist: 
f1_keywords:
 - _STORAGE_BUS_TYPE
 - winioctl/_STORAGE_BUS_TYPE
 - PSTORAGE_BUS_TYPE
 - winioctl/PSTORAGE_BUS_TYPE
 - STORAGE_BUS_TYPE
 - winioctl/STORAGE_BUS_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - STORAGE_BUS_TYPE
---

# STORAGE_BUS_TYPE enumeration


## -description

Specifies the various types of storage buses.

## -enum-fields

### -field BusTypeUnknown:0x00

Unknown bus type.

### -field BusTypeScsi

SCSI bus.

### -field BusTypeAtapi

ATAPI bus.

### -field BusTypeAta

ATA bus.

### -field BusType1394

IEEE-1394 bus.

### -field BusTypeSsa

SSA bus.

### -field BusTypeFibre

Fibre Channel bus.

### -field BusTypeUsb

USB bus.

### -field BusTypeRAID

RAID bus.

### -field BusTypeiScsi

### -field BusTypeSas

Serial Attached SCSI (SAS) bus.

**Windows Server 2003:**  This is not supported before Windows Server 2003 with SP1.

### -field BusTypeSata

SATA bus.

**Windows Server 2003:**  This is not supported before Windows Server 2003 with SP1.

### -field BusTypeSd

### -field BusTypeMmc

### -field BusTypeVirtual

### -field BusTypeFileBackedVirtual

### -field BusTypeSpaces

### -field BusTypeNvme

### -field BusTypeSCM

### -field BusTypeUfs

### -field BusTypeMax

### -field BusTypeMaxReserved:0x7F

### -field BusTypeiSCSI

iSCSI bus.

**Windows Server 2003:**  This is not supported before Windows Server 2003 with SP1.

## -see-also

* [DEVICE_MEDIA_INFO](ns-winioctl-device_media_info.md)

