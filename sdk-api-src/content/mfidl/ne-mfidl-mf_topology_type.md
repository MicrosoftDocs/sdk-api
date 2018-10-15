---
UID: NE:mfidl.MF_TOPOLOGY_TYPE
title: MF_TOPOLOGY_TYPE
author: windows-sdk-content
description: Defines the type of a topology node.
old-location: mf\mf_topology_type.htm
tech.root: medfound
ms.assetid: 73ea1f48-0d86-4104-860c-83a4f9189920
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: 73ea1f48-0d86-4104-860c-83a4f9189920, MF_TOPOLOGY_MAX, MF_TOPOLOGY_OUTPUT_NODE, MF_TOPOLOGY_SOURCESTREAM_NODE, MF_TOPOLOGY_TEE_NODE, MF_TOPOLOGY_TRANSFORM_NODE, MF_TOPOLOGY_TYPE, MF_TOPOLOGY_TYPE enumeration [Media Foundation], mf.mf_topology_type, mfidl/MF_TOPOLOGY_MAX, mfidl/MF_TOPOLOGY_OUTPUT_NODE, mfidl/MF_TOPOLOGY_SOURCESTREAM_NODE, mfidl/MF_TOPOLOGY_TEE_NODE, mfidl/MF_TOPOLOGY_TRANSFORM_NODE, mfidl/MF_TOPOLOGY_TYPE
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
 - MF_TOPOLOGY_TYPE
product: Windows
targetos: Windows
req.typenames: MF_TOPOLOGY_TYPE
req.redist: 
---

# MF_TOPOLOGY_TYPE enumeration


## -description



Defines the type of a topology node.




## -enum-fields




### -field MF_TOPOLOGY_OUTPUT_NODE

Output node. Represents a media sink in the topology.


### -field MF_TOPOLOGY_SOURCESTREAM_NODE

Source node. Represents a media stream in the topology.


### -field MF_TOPOLOGY_TRANSFORM_NODE

Transform node. Represents a Media Foundation Transform (MFT) in the topology.


### -field MF_TOPOLOGY_TEE_NODE

Tee node. A tee node does not hold a pointer to an object. Instead, it represents a fork in the stream. A tee node has one input and multiple outputs, and samples from the upstream node are delivered to all of the downstream nodes.


### -field MF_TOPOLOGY_MAX

Reserved.


## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

