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

# D2D1_TILE_PROP enumeration


## -description



          Identifiers for properties of the <a href="https://msdn.microsoft.com/C7505DBF-5F79-4407-84C4-634EA7EC06B7">Tile effect</a>.
        


## -enum-fields




### -field D2D1_TILE_PROP_RECT


            The region of the image to be tiled. This property is a <a href="https://msdn.microsoft.com/6D931285-0F2B-44BE-8A1A-2348AC49A8DF">D2D1_VECTOR_4F</a> defined as: (left, top, right, bottom). The units are in DIPs.
            

The type is <a href="https://msdn.microsoft.com/6D931285-0F2B-44BE-8A1A-2348AC49A8DF">D2D1_VECTOR_4F</a>.

The default is {0.0f, 0.0f, 100.0f, 100.0f}.


### -field D2D1_TILE_PROP_FORCE_DWORD



