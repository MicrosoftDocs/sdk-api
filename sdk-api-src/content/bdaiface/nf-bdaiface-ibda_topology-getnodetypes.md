---
UID: NF:bdaiface.IBDA_Topology.GetNodeTypes
title: IBDA_Topology::GetNodeTypes
author: windows-sdk-content
description: The GetNodeTypes method retrieves a list of all the node types in the template topology for this filter and network type.
old-location: mstv\ibda_topology_getnodetypes.htm
tech.root: mstv
ms.assetid: 6912cd69-76c2-4dae-bda3-42139acffe4c
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetNodeTypes, GetNodeTypes method [Microsoft TV Technologies], GetNodeTypes method [Microsoft TV Technologies],IBDA_Topology interface, IBDA_Topology interface [Microsoft TV Technologies],GetNodeTypes method, IBDA_Topology.GetNodeTypes, IBDA_Topology::GetNodeTypes, IBDA_TopologyGetNodeTypes, bdaiface/IBDA_Topology::GetNodeTypes, mstv.ibda_topology_getnodetypes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: bdaiface.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_Topology.GetNodeTypes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBDA_Topology::GetNodeTypes


## -description



The <b>GetNodeTypes</b> method retrieves a list of all the node types in the template topology for this filter and network type.




## -parameters




### -param pulcNodeTypes [out]

Pointer that receives the number of node types in the list.


### -param ulcNodeTypesMax [in]

The maximum number of node types that can be held by the <i>rgulNodeTypes</i> buffer.


### -param rgulNodeTypes [out]

Pointer to a buffer that receives the list of node types.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



The <b>IBDA_Topology</b> interface is implemented by a BDA Device Filter. It is used by a Network Provider to query a BDA Device Filter's possible topologies (template topology) and to configure the device with an appropriate topology for the current tuning request. It is also used to get an <b>IUnknown</b> to a control node which may be used to set specific tuning information.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd693447(v=VS.85).aspx">IBDA_Topology Interface</a>
 

 

