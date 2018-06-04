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

# D2D1_COLORMATRIX_ALPHA_MODE enumeration


## -description


The alpha mode of the output of the <a href="https://msdn.microsoft.com/093EEEF1-8C38-414E-8261-58A6C3DD930D">Color matrix effect</a>.


## -enum-fields




### -field D2D1_COLORMATRIX_ALPHA_MODE_PREMULTIPLIED

The effect un-premultiplies the input, applies the color matrix, and premultiplies the output.


### -field D2D1_COLORMATRIX_ALPHA_MODE_STRAIGHT

The effect applies the color matrix directly to the input, and doesn't premultiply the output.


### -field D2D1_COLORMATRIX_ALPHA_MODE_FORCE_DWORD



