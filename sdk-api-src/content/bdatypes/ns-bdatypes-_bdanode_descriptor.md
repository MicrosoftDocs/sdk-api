---
UID: NS:bdatypes._BDANODE_DESCRIPTOR
title: "_BDANODE_DESCRIPTOR"
author: windows-driver-content
description: The BDANODE_DESCRIPTOR structure describes a control node in BDA device filter.
old-location: mstv\bdanode_descriptor.htm
old-project: mstv
ms.assetid: 6ab03494-6564-4d4d-83bf-a9a6e588aac3
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: "*PBDANODE_DESCRIPTOR, BDANODE_DESCRIPTOR, BDANODE_DESCRIPTOR structure [Microsoft TV Technologies], PBDANODE_DESCRIPTOR, PBDANODE_DESCRIPTOR structure pointer [Microsoft TV Technologies], _BDANODE_DESCRIPTOR, bdatypes/BDANODE_DESCRIPTOR, bdatypes/PBDANODE_DESCRIPTOR, mstv.bdanode_descriptor"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: bdatypes.h
req.include-header: 
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
req.typenames: BDANODE_DESCRIPTOR, *PBDANODE_DESCRIPTOR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Bdatypes.h
api_name:
-	BDANODE_DESCRIPTOR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _BDANODE_DESCRIPTOR structure


## -description



The <b>BDANODE_DESCRIPTOR</b> structure describes a control node in BDA device filter.




## -struct-fields




### -field ulBdaNodeType

Specifies the node type as it is used in the BDA template topology. Currently, the only defined node type is NODE_TYPE_PID_MAPPER.


### -field guidFunction

Specifies the function of the node in the topology. Set this parameter to one of the KSNODE_BDA_<i>XXX</i> GUID values in header file Bdamedia.h.


### -field guidName

Specifies a GUID value that can be used to look up a displayable name for the node.


## -remarks



This structure is used by the <a href="https://msdn.microsoft.com/4bbfa1d1-7101-4ca6-b6dc-e66b3c49857d">IBDA_Topology::GetNodeDescriptors</a> method.




## -see-also




<a href="https://msdn.microsoft.com/5ae43ac6-519d-486b-aaa5-c766f3194ef2">BDA Structures</a>
 

 

