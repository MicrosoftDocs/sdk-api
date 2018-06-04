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

# InkPoint function


## -description



          Creates a <a href="https://msdn.microsoft.com/C18E7B04-12B8-4EB9-BAFB-24FBA99210E9">D2D1_INK_POINT</a> structure.
        


## -parameters




### -param point [ref]

Type: <b>const <a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The x and y coordinates of the point.


### -param radius

Type: <b>FLOAT</b>

The radius of this point. Corresponds to the width of the ink stroke at this point in the stroke.


## -returns



Type: <b><a href="https://msdn.microsoft.com/C18E7B04-12B8-4EB9-BAFB-24FBA99210E9">D2D1_INK_POINT</a></b>


            Returns the created <a href="https://msdn.microsoft.com/C18E7B04-12B8-4EB9-BAFB-24FBA99210E9">D2D1_INK_POINT</a> structure.
          




## -see-also




<a href="https://msdn.microsoft.com/C18E7B04-12B8-4EB9-BAFB-24FBA99210E9">D2D1_INK_POINT</a>
 

 

