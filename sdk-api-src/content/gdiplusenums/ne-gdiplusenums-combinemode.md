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

# CombineMode enumeration


## -description


The <b>CombineMode</b> enumeration specifies how a new region is combined with an existing region.


## -enum-fields




### -field CombineModeReplace

Specifies that the existing region is replaced by the new region. 


### -field CombineModeIntersect

Specifies that the existing region is replaced by the intersection of itself and the new region. 


### -field CombineModeUnion

Specifies that the existing region is replaced by the union of itself and the new region. 


### -field CombineModeXor

Specifies that the existing region is replaced by the result of performing an 
				<b>XOR</b> on the two regions. A point is in the 
				<b>XOR</b> of two regions if it is in one region or the other but not in both regions. 


### -field CombineModeExclude

Specifies that the existing region is replaced by the portion of itself that is outside of the new region. 


### -field CombineModeComplement

Specifies that the existing region is replaced by the portion of the new region that is outside of the existing region. 

