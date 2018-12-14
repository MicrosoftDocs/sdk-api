---
UID: NF:bdaiface.IBDA_Topology.GetPinTypes
title: IBDA_Topology::GetPinTypes
author: windows-sdk-content
description: The GetPinTypes method retrieves a list of all the pin types in the template topology for this filter and network type.
old-location: mstv\ibda_topology_getpintypes.htm
tech.root: mstv
ms.assetid: e94c5ae3-1d5f-4ca6-a09b-7190cbe2035b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetPinTypes, GetPinTypes method [Microsoft TV Technologies], GetPinTypes method [Microsoft TV Technologies],IBDA_Topology interface, IBDA_Topology interface [Microsoft TV Technologies],GetPinTypes method, IBDA_Topology.GetPinTypes, IBDA_Topology::GetPinTypes, IBDA_TopologyGetPinTypes, bdaiface/IBDA_Topology::GetPinTypes, mstv.ibda_topology_getpintypes
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
 - IBDA_Topology.GetPinTypes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBDA_Topology::GetPinTypes


## -description



The <b>GetPinTypes</b> method retrieves a list of all the pin types in the template topology for this filter and network type.




## -parameters




### -param pulcPinTypes [out]

Pointer to a value that receives the number of pin types in the list.


### -param ulcPinTypesMax [in]

The maximum number of pin types that can be held by the <i>rgulPinTypes</i> buffer.


### -param rgulPinTypes [out]

Pointer to a buffer to receive the list of pin types.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd693447(v=VS.85).aspx">IBDA_Topology Interface</a>
 

 

