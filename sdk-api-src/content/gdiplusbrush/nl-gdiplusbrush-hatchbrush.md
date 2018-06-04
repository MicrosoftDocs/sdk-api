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

# HatchBrush class


## -description


This <a href="https://msdn.microsoft.com/f1c7c756-12c3-469d-9fe1-03b01f8ac269">HatchBrush</a> class defines a rectangular brush with a hatch style, a foreground color, and a background color. There are six hatch styles. The foreground color defines the color of the hatch lines; the background color defines the color over which the hatch lines are drawn.


## -remarks



Hatches are applied to shape interiors in the device space. As a result, they maintain their appearance in device space and are unaffected by current transformations in the graphics context. Such brushes are also called nonscalable brushes. Hatches are aligned at the upper-left corner of the display device. When the graphics engine uses a <a href="https://msdn.microsoft.com/f1c7c756-12c3-469d-9fe1-03b01f8ac269">HatchBrush</a> object to paint a shape, it first transforms the shape to device space before applying the hatch to the interiors. Hatches are always tiled to paint the interiors.



