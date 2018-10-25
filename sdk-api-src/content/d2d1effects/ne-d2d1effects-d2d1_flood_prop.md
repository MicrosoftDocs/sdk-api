---
UID: NE:d2d1effects.D2D1_FLOOD_PROP
title: D2D1_FLOOD_PROP
author: windows-sdk-content
description: Identifiers for properties of the Flood effect.
old-location: direct2d\d2d1_flood_prop.htm
tech.root: direct2d
ms.assetid: C8132218-70A8-4242-9D10-A2FD08099DD3
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: D2D1_FLOOD_PROP, D2D1_FLOOD_PROP enumeration [Direct2D], D2D1_FLOOD_PROP_COLOR, d2d1effects/D2D1_FLOOD_PROP, d2d1effects/D2D1_FLOOD_PROP_COLOR, direct2d.d2d1_flood_prop
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
 - D2D1_FLOOD_PROP
product: Windows
targetos: Windows
req.typenames: D2D1_FLOOD_PROP
req.redist: 
---

# D2D1_FLOOD_PROP enumeration


## -description


Identifiers for properties of the <a href="https://msdn.microsoft.com/en-us/library/Hh706336(v=VS.85).aspx">Flood effect</a>.
        


## -enum-fields




### -field D2D1_FLOOD_PROP_COLOR

The color and opacity of the bitmap. This property is a D2D1_VECTOR_4F. The individual values for each channel are of type FLOAT, unbounded and unitless.
            The effect doesn't modify the values for the channels.
            

The RGBA values for each channel range from 0 to 1.

The type is <a href="https://msdn.microsoft.com/6D931285-0F2B-44BE-8A1A-2348AC49A8DF">D2D1_VECTOR_4F</a>.

The default value is {0.0f, 0.0f, 0.0f, 1.0f}.


### -field D2D1_FLOOD_PROP_FORCE_DWORD



