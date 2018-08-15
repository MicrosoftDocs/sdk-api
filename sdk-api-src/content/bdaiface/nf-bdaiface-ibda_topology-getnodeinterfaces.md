---
UID: NF:bdaiface.IBDA_Topology.GetNodeInterfaces
title: IBDA_Topology::GetNodeInterfaces
author: windows-sdk-content
description: The GetNodeInterfaces method retrieves a list of the interfaces supported by a node type.
old-location: mstv\ibda_topology_getnodeinterfaces.htm
old-project: mstv
ms.assetid: c3dc4b38-933c-4aeb-b6eb-7273ce334ba2
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetNodeInterfaces, GetNodeInterfaces method [Microsoft TV Technologies], GetNodeInterfaces method [Microsoft TV Technologies],IBDA_Topology interface, IBDA_Topology interface [Microsoft TV Technologies],GetNodeInterfaces method, IBDA_Topology.GetNodeInterfaces, IBDA_Topology::GetNodeInterfaces, IBDA_TopologyGetNodeInterfaces, bdaiface/IBDA_Topology::GetNodeInterfaces, mstv.ibda_topology_getnodeinterfaces
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bdaiface.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: UICloseReasonType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_Topology.GetNodeInterfaces
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_Topology::GetNodeInterfaces


## -description



The <b>GetNodeInterfaces</b> method retrieves a list of the interfaces supported by a node type.




## -parameters




### -param ulNodeType [in]

Specifies the node type for which the interface list is being requested.


### -param pulcInterfaces [out]

Pointer that receives the number of interfaces in the list.


### -param ulcInterfacesMax [in]

Specifies the maximum number of interfaces that <i>rgguidInterfaces</i> can hold.


### -param rgguidInterfaces [out]

Pointer to a buffer that holds the list of interface GUIDs.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/35dfe39e-05b4-4c7b-9358-081429b064f2">IBDA_Topology Interface</a>
 

 

