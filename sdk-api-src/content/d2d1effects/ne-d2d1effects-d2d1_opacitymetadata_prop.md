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

# D2D1_OPACITYMETADATA_PROP enumeration


## -description



          Identifiers for properties of the <a href="https://msdn.microsoft.com/25B34A31-8533-4339-BBF7-2D7E5488E301">Opacity metadata effect</a>.
        


## -enum-fields




### -field D2D1_OPACITYMETADATA_PROP_INPUT_OPAQUE_RECT

The portion of the source image that is opaque. The default is the entire input image.
          

The type is <a href="https://msdn.microsoft.com/6D931285-0F2B-44BE-8A1A-2348AC49A8DF">D2D1_VECTOR_4F</a>.

The default is {-FLT_MAX, -FLT_MAX, FLT_MAX, FLT_MAX}.


### -field D2D1_OPACITYMETADATA_PROP_FORCE_DWORD



