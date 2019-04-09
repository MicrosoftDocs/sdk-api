---
UID: NS:winioctl._STORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR
title: STORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR (winioctl.h)
author: windows-sdk-content
description: The STORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR structure is one of the query result structures returned from an IOCTL_STORAGE_QUERY_PROPERTY request.
old-location: fs\storage_physical_topology_descriptor.htm
tech.root: FileIO
ms.assetid: CD596355-228D-4054-B77F-83F323AB3D0B
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PSTORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR, PSTORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR, PSTORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR structure pointer [Files], STORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR, STORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR structure [Files], fs.storage_physical_topology_descriptor, winioctl/PSTORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR, winioctl/STORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR"
ms.topic: struct
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
 - STORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR
product: Windows
targetos: Windows
req.typenames: STORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR, *PSTORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR
req.redist: 
---

# STORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR structure


## -description


The <b>STORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR</b> structure is one of the query result structures returned from an <a href="https://msdn.microsoft.com/6755dcd4-e4a0-423f-9dcc-b9719c8e5c88">IOCTL_STORAGE_QUERY_PROPERTY</a> request. This structure describes storage device physical topology.


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

 




#### - Node[ANYSIZE_ARRAY]

A node as specified by a <a href="https://msdn.microsoft.com/66B5C1F8-A741-4CAD-B717-CB91B0D5655F">STORAGE_PHYSICAL_NODE_DATA</a> structure.

