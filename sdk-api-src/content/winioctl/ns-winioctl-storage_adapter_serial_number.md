---
UID: NS:winioctl._STORAGE_ADAPTER_SERIAL_NUMBER
title: STORAGE_ADAPTER_SERIAL_NUMBER
description: The NULL-terminated Unicode string of the adapter serial number for the StorageAdapterSerialNumberProperty as defined in STORAGE_PROPERTY_ID.
helpviewer_keywords: ["*PSTORAGE_ADAPTER_SERIAL_NUMBER","PSTORAGE_ADAPTER_SERIAL_NUMBER","PSTORAGE_ADAPTER_SERIAL_NUMBER structure pointer [Files]","STORAGE_ADAPTER_SERIAL_NUMBER","STORAGE_ADAPTER_SERIAL_NUMBER structure [Files]","fs.storage_adapter_serial_number","winioctl/PSTORAGE_ADAPTER_SERIAL_NUMBER","winioctl/STORAGE_ADAPTER_SERIAL_NUMBER"]
tech.root: fs
ms.date: 08/19/2020
ms.keywords: '*PSTORAGE_ADAPTER_SERIAL_NUMBER,PSTORAGE_ADAPTER_SERIAL_NUMBER,PSTORAGE_ADAPTER_SERIAL_NUMBER structure pointer [Files],STORAGE_ADAPTER_SERIAL_NUMBER,STORAGE_ADAPTER_SERIAL_NUMBER structure [Files],fs.storage_adapter_serial_number,winioctl/PSTORAGE_ADAPTER_SERIAL_NUMBER,winioctl/STORAGE_ADAPTER_SERIAL_NUMBER'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
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
req.typenames: _STORAGE_ADAPTER_SERIAL_NUMBER, *P_STORAGE_ADAPTER_SERIAL_NUMBER
req.redist: 
f1_keywords:
 - _STORAGE_ADAPTER_SERIAL_NUMBER
 - winioctl/_STORAGE_ADAPTER_SERIAL_NUMBER
 - PSTORAGE_ADAPTER_SERIAL_NUMBER
 - winioctl/PSTORAGE_ADAPTER_SERIAL_NUMBER
 - STORAGE_ADAPTER_SERIAL_NUMBER
 - winioctl/STORAGE_ADAPTER_SERIAL_NUMBER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winioctl.h
api_name:
 - STORAGE_ADAPTER_SERIAL_NUMBER
---

# _STORAGE_ADAPTER_SERIAL_NUMBER structure


## -description

The NULL-terminated Unicode string of the adapter serial number for the StorageAdapterSerialNumberProperty as defined in [STORAGE_PROPERTY_ID](ne-winioctl-storage_property_id.md).

## -struct-fields

### -field Version

The version of this structure. The Size serves as the version.

### -field Size

The size of this structure.

### -field SerialNumber

The serial number.

