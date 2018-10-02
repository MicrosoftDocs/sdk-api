---
UID: NS:winioctl._STORAGE_PHYSICAL_NODE_DATA
title: "_STORAGE_PHYSICAL_NODE_DATA"
author: windows-sdk-content
description: Specifies the physical device data of a storage node.
old-location: fs\storage_physical_node_data.htm
tech.root: fileio
ms.assetid: 66B5C1F8-A741-4CAD-B717-CB91B0D5655F
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: "*PSTORAGE_PHYSICAL_NODE_DATA, PSTORAGE_PHYSICAL_NODE_DATA, PSTORAGE_PHYSICAL_NODE_DATA structure pointer [Files], STORAGE_PHYSICAL_NODE_DATA, STORAGE_PHYSICAL_NODE_DATA structure [Files], _STORAGE_PHYSICAL_NODE_DATA, fs.storage_physical_node_data, winioctl/PSTORAGE_PHYSICAL_NODE_DATA, winioctl/STORAGE_PHYSICAL_NODE_DATA"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winioctl.h
api_name:
 - STORAGE_PHYSICAL_NODE_DATA
product: Windows
targetos: Windows
req.typenames: STORAGE_PHYSICAL_NODE_DATA, *PSTORAGE_PHYSICAL_NODE_DATA
req.redist: 
---

# _STORAGE_PHYSICAL_NODE_DATA structure


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

The data offset from the beginning of the data structure. The buffer contains an array of <a href="https://msdn.microsoft.com/8CC7CF43-61C8-4561-BA9C-473878818858">STORAGE_PHYSICAL_ADAPTER_DATA</a>.


### -field DeviceCount

A value less than or equal to 1.


### -field DeviceDataLength

The data length of the storage device in the storage node,  in units of kilobytes (1024 bytes).


### -field DeviceDataOffset

The data offset from the beginning of the data structure. The buffer contains an array of <a href="https://msdn.microsoft.com/4B484F79-DDC8-4671-90EA-D793EA0A05C7">STORAGE_PHYSICAL_DEVICE_DATA</a>.


### -field Reserved

 




#### - Reserved[3]

Specifies if the storage adapter is reserved.

