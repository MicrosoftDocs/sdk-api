---
UID: NF:bdaiface.IBDA_Topology.GetNodeDescriptors
title: IBDA_Topology::GetNodeDescriptors (bdaiface.h)

description: The GetNodeDescriptors method retrieves a list of descriptors for the nodes in the topology.
old-location: mstv\ibda_topology_getnodedescriptors.htm
tech.root: mstv
ms.assetid: 4bbfa1d1-7101-4ca6-b6dc-e66b3c49857d

ms.date: 12/05/2018
ms.keywords: GetNodeDescriptors, GetNodeDescriptors method [Microsoft TV Technologies], GetNodeDescriptors method [Microsoft TV Technologies],IBDA_Topology interface, IBDA_Topology interface [Microsoft TV Technologies],GetNodeDescriptors method, IBDA_Topology.GetNodeDescriptors, IBDA_Topology::GetNodeDescriptors, IBDA_TopologyGetNodeDescriptors, bdaiface/IBDA_Topology::GetNodeDescriptors, mstv.ibda_topology_getnodedescriptors
ms.topic: method
f1_keywords: 
 - "bdaiface/IBDA_Topology.GetNodeDescriptors"
dev_langs:
 - c++
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
 - Bdaiface.h
api_name:
 - IBDA_Topology.GetNodeDescriptors
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBDA_Topology::GetNodeDescriptors


## -description



The <b>GetNodeDescriptors</b> method retrieves a list of descriptors for the nodes in the topology.




## -parameters




### -param ulcNodeDescriptors [in, out]

Receives a count of the number of node descriptors written to the <i>rgNodeDescriptors</i> array.


### -param ulcNodeDescriptorsMax [in]

Specifies the maximum number of node descriptors that the <i>rgNodeDescriptors</i> array can hold.


### -param rgNodeDescriptors [in, out]

Pointer to a buffer that receives an array of node descriptors. Each node descriptor is a structure of type <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bdanode-descriptor">BDANODE_DESCRIPTOR</a>.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nn-bdaiface-ibda_topology">IBDA_Topology Interface</a>
 

 

