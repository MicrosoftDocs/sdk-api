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

# D2D1_ATLAS_PROP enumeration


## -description



          Identifiers for properties of the <a href="https://msdn.microsoft.com/D35E32CB-4DF7-408F-A717-1E421DDC8763">Atlas effect</a>.
        


## -enum-fields




### -field D2D1_ATLAS_PROP_INPUT_RECT


            The portion of the image passed to the next effect.
            Type is D2D1_VECTOR_4F.
            Default value is (-FLT_MAX, -FLT_MAX, FLT_MAX, FLT_MAX).
          


### -field D2D1_ATLAS_PROP_INPUT_PADDING_RECT


            The maximum size sampled for the output rectangle.
            Type is D2D1_VECTOR_4F.
            Default value is (-FLT_MAX, -FLT_MAX, FLT_MAX, FLT_MAX).
          


### -field D2D1_ATLAS_PROP_FORCE_DWORD



