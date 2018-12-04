---
UID: NF:bdaiface.IBDA_Topology.CreatePin
title: IBDA_Topology::CreatePin
author: windows-sdk-content
description: The CreatePin method creates an instance of a specified pin type.
old-location: mstv\ibda_topology_createpin.htm
tech.root: mstv
ms.assetid: ced0f8a8-7a34-4357-8795-491e60a22e91
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CreatePin, CreatePin method [Microsoft TV Technologies], CreatePin method [Microsoft TV Technologies],IBDA_Topology interface, IBDA_Topology interface [Microsoft TV Technologies],CreatePin method, IBDA_Topology.CreatePin, IBDA_Topology::CreatePin, IBDA_TopologyCreatePin, bdaiface/IBDA_Topology::CreatePin, mstv.ibda_topology_createpin
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
 - IBDA_Topology.CreatePin
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBDA_Topology::CreatePin


## -description



The <b>CreatePin</b> method creates an instance of a specified pin type.




## -parameters




### -param ulPinType [in]

Specifies the type of pin to create. To obtain the available values, call <a href="https://msdn.microsoft.com/e94c5ae3-1d5f-4ca6-a09b-7190cbe2035b">IBDA_Topology::GetPinTypes</a>.


### -param pulPinId [out]

Pointer that receives the identifier for the new pin.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/35dfe39e-05b4-4c7b-9358-081429b064f2">IBDA_Topology Interface</a>
 

 

