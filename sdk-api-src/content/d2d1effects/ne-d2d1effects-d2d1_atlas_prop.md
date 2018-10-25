---
UID: NE:d2d1effects.D2D1_ATLAS_PROP
title: D2D1_ATLAS_PROP
author: windows-sdk-content
description: Identifiers for properties of the Atlas effect.
old-location: direct2d\d2d1_atlas_prop.htm
tech.root: direct2d
ms.assetid: 7450C113-F1F0-433C-928B-19B0FF21B69B
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: D2D1_ATLAS_PROP, D2D1_ATLAS_PROP enumeration [Direct2D], D2D1_ATLAS_PROP_INPUT_PADDING_RECT, D2D1_ATLAS_PROP_INPUT_RECT, d2d1effects/D2D1_ATLAS_PROP, d2d1effects/D2D1_ATLAS_PROP_INPUT_PADDING_RECT, d2d1effects/D2D1_ATLAS_PROP_INPUT_RECT, direct2d.d2d1_atlas_prop
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d2d1effects.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1effects.h
api_name:
 - D2D1_ATLAS_PROP
product: Windows
targetos: Windows
req.typenames: D2D1_ATLAS_PROP
req.redist: 
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



