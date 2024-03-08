---
UID: NS:winioctl._STORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR
title: STORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR
description: The STORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR structure is one of the query result structures returned from an IOCTL_STORAGE_QUERY_PROPERTY request.
helpviewer_keywords: ["*PSTORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR","PSTORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR","PSTORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR structure pointer [Files]","STORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR","STORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR structure [Files]","fs.storage_physical_topology_descriptor","winioctl/PSTORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR","winioctl/STORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR"]
old-location: fs\storage_physical_topology_descriptor.htm
tech.root: fs
ms.assetid: CD596355-228D-4054-B77F-83F323AB3D0B
ms.date: 12/05/2018
ms.keywords: '*PSTORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR, PSTORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR, PSTORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR structure pointer [Files], STORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR, STORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR structure [Files], fs.storage_physical_topology_descriptor, winioctl/PSTORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR, winioctl/STORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR'
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
targetos: Windows
req.typenames: STORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR, *PSTORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR
req.redist: 
f1_keywords:
 - _STORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR
 - winioctl/_STORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR
 - PSTORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR
 - winioctl/PSTORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR
 - STORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR
 - winioctl/STORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR
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
 - STORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR
---

# STORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR structure


## -description

The <b>STORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR</b> structure is one of the query result structures returned from an <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a> request. This structure describes storage device physical topology.

## -struct-fields

### -field Version

Contains the size of this structure, in bytes. Set to <code>sizeof(STORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR)</code>.

### -field Size

Specifies the total size of the data, in bytes. Should be &gt;= <code>sizeof(STORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR)</code>.

### -field NodeCount

Specifies the number of nodes.

### -field Reserved

Reserved.

### -field Node

A node as specified by a <a href="/windows/desktop/api/winioctl/ns-winioctl-storage_physical_node_data">STORAGE_PHYSICAL_NODE_DATA</a> structure.
