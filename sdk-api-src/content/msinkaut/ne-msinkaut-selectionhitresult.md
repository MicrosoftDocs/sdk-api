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

# SelectionHitResult enumeration


## -description



Specifies which part of a selection, if any, was hit during a hit test.




## -enum-fields




### -field SHR_None

No part of the selection was hit.


### -field SHR_NW

The northwest corner sizing handle was hit.


### -field SHR_SE

The southeast corner sizing handle was hit.


### -field SHR_NE

The northeast corner sizing handle was hit.


### -field SHR_SW

That the southwest corner sizing handle was hit.


### -field SHR_E

The east side sizing handle was hit.


### -field SHR_W

The west side sizing handle was hit.


### -field SHR_N

The north side sizing handle was hit.


### -field SHR_S

The south side sizing handle was hit.


### -field SHR_Selection

The selection itself was hit (no selection handle was hit).


## -see-also




<a href="https://msdn.microsoft.com/289589fa-84da-40b3-b60e-551ef0114279">HitTestSelection Method [InkOverlay Class]</a>



<a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay Class</a>



<a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture Control Reference</a>
 

 

