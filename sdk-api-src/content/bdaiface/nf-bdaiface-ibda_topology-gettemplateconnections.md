---
UID: NF:bdaiface.IBDA_Topology.GetTemplateConnections
title: IBDA_Topology::GetTemplateConnections
author: windows-sdk-content
description: The GetTemplateConnections method retrieves a list of all template connections that appear in the template topology for this filter and network type.
old-location: mstv\ibda_topology_gettemplateconnections.htm
tech.root: mstv
ms.assetid: eeceee7f-8e0f-4852-a69d-eced9772df1a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetTemplateConnections, GetTemplateConnections method [Microsoft TV Technologies], GetTemplateConnections method [Microsoft TV Technologies],IBDA_Topology interface, IBDA_Topology interface [Microsoft TV Technologies],GetTemplateConnections method, IBDA_Topology.GetTemplateConnections, IBDA_Topology::GetTemplateConnections, IBDA_TopologyGetTemplateConnections, bdaiface/IBDA_Topology::GetTemplateConnections, mstv.ibda_topology_gettemplateconnections
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
 - IBDA_Topology.GetTemplateConnections
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBDA_Topology::GetTemplateConnections


## -description



The <b>GetTemplateConnections</b> method retrieves a list of all template connections that appear in the template topology for this filter and network type.




## -parameters




### -param pulcConnections [out]

Pointer to a value to receive the number of connections in the list.


### -param ulcConnectionsMax [in]

The maximum number of connections that can be held by the <i>rgConnections</i> buffer.


### -param rgConnections [out]

Pointer to a buffer that receives the list of connections.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd693447(v=VS.85).aspx">IBDA_Topology Interface</a>
 

 

