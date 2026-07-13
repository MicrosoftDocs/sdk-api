---
UID: NS:winioctl._STORAGE_PHYSICAL_NODE_DATA
title: STORAGE_PHYSICAL_NODE_DATA
description: Specifies the physical device data of a storage node.
helpviewer_keywords: ["*PSTORAGE_PHYSICAL_NODE_DATA","PSTORAGE_PHYSICAL_NODE_DATA","PSTORAGE_PHYSICAL_NODE_DATA structure pointer [Files]","STORAGE_PHYSICAL_NODE_DATA","STORAGE_PHYSICAL_NODE_DATA structure [Files]","fs.storage_physical_node_data","winioctl/PSTORAGE_PHYSICAL_NODE_DATA","winioctl/STORAGE_PHYSICAL_NODE_DATA"]
old-location: fs\storage_physical_node_data.htm
tech.root: fs
ms.assetid: 66B5C1F8-A741-4CAD-B717-CB91B0D5655F
ms.date: 12/05/2018
ms.keywords: '*PSTORAGE_PHYSICAL_NODE_DATA, PSTORAGE_PHYSICAL_NODE_DATA, PSTORAGE_PHYSICAL_NODE_DATA structure pointer [Files], STORAGE_PHYSICAL_NODE_DATA, STORAGE_PHYSICAL_NODE_DATA structure [Files], fs.storage_physical_node_data, winioctl/PSTORAGE_PHYSICAL_NODE_DATA, winioctl/STORAGE_PHYSICAL_NODE_DATA'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: STORAGE_PHYSICAL_NODE_DATA, *PSTORAGE_PHYSICAL_NODE_DATA
req.redist: 
f1_keywords:
 - _STORAGE_PHYSICAL_NODE_DATA
 - winioctl/_STORAGE_PHYSICAL_NODE_DATA
 - PSTORAGE_PHYSICAL_NODE_DATA
 - winioctl/PSTORAGE_PHYSICAL_NODE_DATA
 - STORAGE_PHYSICAL_NODE_DATA
 - winioctl/STORAGE_PHYSICAL_NODE_DATA
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
 - STORAGE_PHYSICAL_NODE_DATA
---

# STORAGE_PHYSICAL_NODE_DATA structure


## -description

Specifies the physical device data of a storage node.

## -struct-fields

### -field NodeId

The hardware ID of the storage node.

### -field AdapterCount

A value of 0 or 1 that indicates the adapter count in the storage node.

### -field AdapterDataLength

The data length of the storage adapter in the storage node,  in units of kilobytes (1024 bytes).

### -field AdapterDataOffset

The data offset from the beginning of the data structure. The buffer contains an array of <a href="/windows/desktop/api/winioctl/ns-winioctl-storage_physical_adapter_data">STORAGE_PHYSICAL_ADAPTER_DATA</a>.

### -field DeviceCount

A value less than or equal to 1.

### -field DeviceDataLength

The data length of the storage device in the storage node,  in units of kilobytes (1024 bytes).

### -field DeviceDataOffset

The data offset from the beginning of the data structure. The buffer contains an array of <a href="/windows/desktop/api/winioctl/ns-winioctl-storage_physical_device_data">STORAGE_PHYSICAL_DEVICE_DATA</a>.

### -field Reserved

Specifies if the storage adapter is reserved.
