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

# D2D1_INK_BEZIER_SEGMENT structure


## -description


Represents a Bezier segment to be used in the creation of an <a href="https://msdn.microsoft.com/4B6DD4C2-8E91-4AEA-AFB5-21B4FD13F75A">ID2D1Ink</a> object. 
        This structure differs from <a href="https://msdn.microsoft.com/cf8df7d2-c4fe-4a46-a4b2-7e0eed67df2a">D2D1_BEZIER_SEGMENT</a> in that it is composed 
        of <a href="https://msdn.microsoft.com/C18E7B04-12B8-4EB9-BAFB-24FBA99210E9">D2D1_INK_POINT</a>s, which contain a radius in addition to x- and y-coordinates.
        


## -struct-fields




### -field point1

The first control point for the Bezier segment.


### -field point2

The second control point for the Bezier segment.


### -field point3

The end point for the Bezier segment.

