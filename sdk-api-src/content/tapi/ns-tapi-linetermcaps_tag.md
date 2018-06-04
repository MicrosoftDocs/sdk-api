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

# linetermcaps_tag structure


## -description


The 
<b>LINETERMCAPS</b> structure describes the capabilities of a line's terminal device. The 
<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a> structure can contain an array of 
<b>LINETERMCAPS</b> structures.


## -struct-fields




### -field dwTermDev

Device type of the terminal. This member uses one of the 
<a href="https://msdn.microsoft.com/3444d022-8225-4956-89a1-721b4662d557">LINETERMDEV_ Constants</a>.


### -field dwTermModes

Terminal mode(s) the terminal device is able to deal with. This member uses one of the 
<a href="https://msdn.microsoft.com/60af1687-8958-4918-be21-a13780c60974">LINETERMMODE_ Constants</a>.


### -field dwTermSharing

Sharing modes for the terminal device. This member uses one of the 
<a href="https://msdn.microsoft.com/50a52a50-4d94-4068-9ea4-bea862400036">LINETERMSHARING_ Constants</a>.


## -remarks



This structure may not be extended.




## -see-also




<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a>



<a href="https://msdn.microsoft.com/6c5a668e-9a9a-4a7a-98e9-bd8ec4b819b2">TSPI_lineGetDevCaps</a>



<a href="https://msdn.microsoft.com/c0900c5b-8791-4653-8bfc-d32e51d10c50">lineGetDevCaps</a>



<a href="https://msdn.microsoft.com/362114d9-c5b6-4b78-bb31-811eb89fe82d">lineSetTerminal</a>
 

 

