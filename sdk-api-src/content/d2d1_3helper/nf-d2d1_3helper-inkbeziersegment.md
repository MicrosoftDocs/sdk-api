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

# InkBezierSegment function


## -description



          Creates a <a href="https://msdn.microsoft.com/27F1F78B-2478-4F5D-BF56-9931E767C358">D2D1_INK_BEZIER_SEGMENT</a> structure.
        


## -parameters




### -param point1 [ref]

Type: <b>const <a href="https://msdn.microsoft.com/C18E7B04-12B8-4EB9-BAFB-24FBA99210E9">D2D1_INK_POINT</a></b>

The first control point for the Bezier segment.


### -param point2 [ref]

Type: <b>const <a href="https://msdn.microsoft.com/C18E7B04-12B8-4EB9-BAFB-24FBA99210E9">D2D1_INK_POINT</a></b>

The second control point for the Bezier segment.


### -param point3 [ref]

Type: <b>const <a href="https://msdn.microsoft.com/C18E7B04-12B8-4EB9-BAFB-24FBA99210E9">D2D1_INK_POINT</a></b>

The end point for the Bezier segment.


## -returns



Type: <b><a href="https://msdn.microsoft.com/27F1F78B-2478-4F5D-BF56-9931E767C358">D2D1_INK_BEZIER_SEGMENT</a></b>


            Returns the created <a href="https://msdn.microsoft.com/27F1F78B-2478-4F5D-BF56-9931E767C358">D2D1_INK_BEZIER_SEGMENT</a> structure.
          




## -see-also




<a href="https://msdn.microsoft.com/27F1F78B-2478-4F5D-BF56-9931E767C358">D2D1_INK_BEZIER_SEGMENT</a>
 

 

