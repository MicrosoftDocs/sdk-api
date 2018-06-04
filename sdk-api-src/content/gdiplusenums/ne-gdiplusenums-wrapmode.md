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

# WrapMode enumeration


## -description


The <b>WrapMode</b> enumeration specifies how repeated copies of an image are used to tile an area.


## -enum-fields




### -field WrapModeTile

Specifies tiling without flipping. 


### -field WrapModeTileFlipX

Specifies that tiles are flipped horizontally as you move from one tile to the next in a row. 


### -field WrapModeTileFlipY

Specifies that tiles are flipped vertically as you move from one tile to the next in a column. 


### -field WrapModeTileFlipXY

Specifies that tiles are flipped horizontally as you move along a row and flipped vertically as you move along a column. 


### -field WrapModeClamp

Specifies that no tiling takes place. 

