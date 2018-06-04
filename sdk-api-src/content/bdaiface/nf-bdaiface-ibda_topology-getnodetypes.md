---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/35dfe39e-05b4-4c7b-9358-081429b064f2">IBDA_Topology Interface</a>
 

 

