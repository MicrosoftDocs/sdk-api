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

# D2D1_FLOOD_PROP enumeration


## -description



          Identifiers for properties of the <a href="https://msdn.microsoft.com/F80A6DC0-E18C-4324-BE4A-FE40C5722988">Flood effect</a>.
        


## -enum-fields




### -field D2D1_FLOOD_PROP_COLOR


            The color and opacity of the bitmap. This property is a D2D1_VECTOR_4F. The individual values for each channel are of type FLOAT, unbounded and unitless.
            The effect doesn't modify the values for the channels.
            

The RGBA values for each channel range from 0 to 1.

The type is <a href="https://msdn.microsoft.com/6D931285-0F2B-44BE-8A1A-2348AC49A8DF">D2D1_VECTOR_4F</a>.

The default value is {0.0f, 0.0f, 0.0f, 1.0f}.


### -field D2D1_FLOOD_PROP_FORCE_DWORD



