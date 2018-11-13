---
UID: NE:winioctl._STORAGE_BUS_TYPE
title: "_STORAGE_BUS_TYPE"
author: windows-sdk-content
description: Provides a symbolic means of representing storage bus types.
old-location: fs\storage_bus_type.htm
tech.root: fileio
ms.assetid: 3c915e05-3974-4f62-b410-b28eddea129a
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: "*PSTORAGE_BUS_TYPE, BusType1394, BusTypeAta, BusTypeAtapi, BusTypeFibre, BusTypeFileBackedVirtual, BusTypeMax, BusTypeMaxReserved, BusTypeMmc, BusTypeRAID, BusTypeSas, BusTypeSata, BusTypeScsi, BusTypeSd, BusTypeSsa, BusTypeUnknown, BusTypeUsb, BusTypeVirtual, BusTypeiScsi, PSTORAGE_BUS_TYPE, PSTORAGE_BUS_TYPE enumeration pointer [Files], STORAGE_BUS_TYPE, STORAGE_BUS_TYPE enumeration [Files], _STORAGE_BUS_TYPE, fs.storage_bus_type, winioctl/BusType1394, winioctl/BusTypeAta, winioctl/BusTypeAtapi, winioctl/BusTypeFibre, winioctl/BusTypeFileBackedVirtual, winioctl/BusTypeMax, winioctl/BusTypeMaxReserved, winioctl/BusTypeMmc, winioctl/BusTypeRAID, winioctl/BusTypeSas, winioctl/BusTypeSata, winioctl/BusTypeScsi, winioctl/BusTypeSd, winioctl/BusTypeSsa, winioctl/BusTypeUnknown, winioctl/BusTypeUsb, winioctl/BusTypeVirtual, winioctl/BusTypeiScsi, winioctl/PSTORAGE_BUS_TYPE, winioctl/STORAGE_BUS_TYPE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: winioctl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - STORAGE_BUS_TYPE
product: Windows
targetos: Windows
req.typenames: STORAGE_BUS_TYPE, *PSTORAGE_BUS_TYPE
req.redist: 
---

# _STORAGE_BUS_TYPE enumeration


## -description


Provides a symbolic means of representing storage bus types.


## -enum-fields




### -field BusTypeUnknown

Indicates an unknown bus type.


### -field BusTypeScsi

Indicates a SCSI bus type.


### -field BusTypeAtapi

Indicates an ATAPI bus type.


### -field BusTypeAta

Indicates an ATA bus type.


### -field BusType1394

Indicates an IEEE 1394 bus type.


### -field BusTypeSsa

Indicates an SSA bus type.


### -field BusTypeFibre

Indicates a fiber channel bus type.


### -field BusTypeUsb

Indicates a USB bus type.


### -field BusTypeRAID

Indicates a RAID bus type.


### -field BusTypeiScsi

Indicates an iSCSI bus type.

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported before Windows Vista and Windows Server 2008.


### -field BusTypeSas

Indicates a serial-attached SCSI (SAS) bus type.

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported before Windows Vista and Windows Server 2008.


### -field BusTypeSata

Indicates a SATA bus type.

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported before Windows Vista and Windows Server 2008.


### -field BusTypeSd

Indicates a secure digital (SD) bus type.

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported before Windows Vista and Windows Server 2008.


### -field BusTypeMmc

Indicates a multimedia card (MMC) bus type.

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported before Windows Vista and Windows Server 2008.


### -field BusTypeVirtual

Indicates a virtual bus type.

<b>Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported before Windows 7 and Windows Server 2008.


### -field BusTypeFileBackedVirtual

Indicates a file-backed virtual bus type.

<b>Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported before Windows 7 and Windows Server 2008.


### -field BusTypeSpaces


### -field BusTypeNvme


### -field BusTypeSCM


### -field BusTypeUfs


### -field BusTypeMax

Indicates the maximum value for this value.


### -field BusTypeMaxReserved

The maximum value of the storage bus type range.


## -see-also




<a href="https://msdn.microsoft.com/ed8fe5c1-dbdf-43bc-a0a7-17e541eba950">Disk Management Enumeration Types</a>
 

 

