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

# DWRITE_OVERHANG_METRICS structure


## -description


Indicates how much any visible DIPs (device independent pixels) overshoot each side of the layout or inline objects.

Positive overhangs indicate that the visible area extends outside the layout box or inline object, while negative values mean there is whitespace inside.
 The returned values are unaffected by rendering transforms or pixel snapping.  Additionally, they may not exactly match the final target's pixel bounds after applying grid fitting and hinting.


## -struct-fields




### -field left

Type: <b>FLOAT</b>

The distance from the left-most visible DIP to its  left-alignment edge.


### -field top

Type: <b>FLOAT</b>

The distance from the top-most visible DIP to its  top alignment edge.


### -field right

Type: <b>FLOAT</b>

The distance from the right-most visible DIP to its  right-alignment edge.


### -field bottom

Type: <b>FLOAT</b>

The distance from the bottom-most visible DIP to its lower-alignment edge.

