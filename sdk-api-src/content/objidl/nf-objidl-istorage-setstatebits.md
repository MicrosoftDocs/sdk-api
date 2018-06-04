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

# IStorage::SetStateBits


## -description


The <b>SetStateBits</b> method stores up to 32 bits of state information in this storage object. This method is reserved for future use.


## -parameters




### -param grfStateBits [in]

Specifies the new values of the bits to set. No legal values are defined for these bits; they are all reserved for future use and must not be used by applications.


### -param grfMask [in]

A binary mask indicating which bits in <i>grfStateBits</i> are significant in this call.


## -returns



This method can return one of these values.




## -remarks



The values for the state bits are not currently defined.




## -see-also




<a href="https://msdn.microsoft.com/2a2253f6-d3d3-403e-a9ba-53a541c7a31e">IStorage - Compound File Implementation</a>



<a href="https://msdn.microsoft.com/87478fa8-1b5f-44ed-bffc-e139c7f44a12">IStorage::Stat</a>
 

 

