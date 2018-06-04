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

# DWRITE_MEASURING_MODE enumeration


## -description



        Indicates the measuring method used for text layout.


## -enum-fields




### -field DWRITE_MEASURING_MODE_NATURAL


            
            Specifies that text is measured using glyph ideal metrics whose values are independent to the current display resolution.


### -field DWRITE_MEASURING_MODE_GDI_CLASSIC


            
            Specifies that text is measured using glyph display-compatible metrics whose values tuned for the current display resolution.


### -field DWRITE_MEASURING_MODE_GDI_NATURAL


            
            Specifies that text is measured using the same glyph display metrics as text measured by GDI using a font created with CLEARTYPE_NATURAL_QUALITY.

