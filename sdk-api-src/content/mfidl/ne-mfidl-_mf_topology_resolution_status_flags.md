---
UID: NE:mfidl._MF_TOPOLOGY_RESOLUTION_STATUS_FLAGS
title: "_MF_TOPOLOGY_RESOLUTION_STATUS_FLAGS"
author: windows-sdk-content
description: Defines status flags for the MF_TOPOLOGY_RESOLUTION_STATUS attribute.
old-location: mf\mf_topology_resolution_status_flags.htm
tech.root: medfound
ms.assetid: e2746378-cf01-4a41-af02-9c3089671120
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: MF_OPTIONAL_NODE_REJECTED_MEDIA_TYPE, MF_OPTIONAL_NODE_REJECTED_PROTECTED_PROCESS, MF_TOPOLOGY_RESOLUTION_STATUS_FLAGS, MF_TOPOLOGY_RESOLUTION_STATUS_FLAGS enumeration [Media Foundation], MF_TOPOLOGY_RESOLUTION_SUCCEEDED, _MF_TOPOLOGY_RESOLUTION_STATUS_FLAGS, e2746378-cf01-4a41-af02-9c3089671120, mf.mf_topology_resolution_status_flags, mfidl/MF_OPTIONAL_NODE_REJECTED_MEDIA_TYPE, mfidl/MF_OPTIONAL_NODE_REJECTED_PROTECTED_PROCESS, mfidl/MF_TOPOLOGY_RESOLUTION_STATUS_FLAGS, mfidl/MF_TOPOLOGY_RESOLUTION_SUCCEEDED
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - mfidl.h
api_name:
 - MF_TOPOLOGY_RESOLUTION_STATUS_FLAGS
product: Windows
targetos: Windows
req.typenames: MF_TOPOLOGY_RESOLUTION_STATUS_FLAGS
req.redist: 
---

# _MF_TOPOLOGY_RESOLUTION_STATUS_FLAGS enumeration


## -description



Defines status flags for the <a href="https://msdn.microsoft.com/7c2410ce-e70b-4303-9dbc-caff4a355d6b">MF_TOPOLOGY_RESOLUTION_STATUS</a> attribute.




## -enum-fields




### -field MF_TOPOLOGY_RESOLUTION_SUCCEEDED

The topology was resolved successfully.


### -field MF_OPTIONAL_NODE_REJECTED_MEDIA_TYPE

An optional topology node was rejected because the topology loader could not find a media type for the connection.


### -field MF_OPTIONAL_NODE_REJECTED_PROTECTED_PROCESS

An optional topology node was rejected because it could not be loaded into a protected process.


## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

