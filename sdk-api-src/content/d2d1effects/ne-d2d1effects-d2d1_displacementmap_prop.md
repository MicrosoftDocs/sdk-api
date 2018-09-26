---
UID: NE:d2d1effects.D2D1_DISPLACEMENTMAP_PROP
title: D2D1_DISPLACEMENTMAP_PROP
author: windows-sdk-content
description: Identifiers for properties of the Displacement map effect.
old-location: direct2d\d2d1_displacementmap_prop.htm
tech.root: direct2d
ms.assetid: 29DD521D-3CFE-400B-BA9F-6EFEF0DC6BB7
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: D2D1_DISPLACEMENTMAP_PROP, D2D1_DISPLACEMENTMAP_PROP enumeration [Direct2D], D2D1_DISPLACEMENTMAP_PROP_SCALE, D2D1_DISPLACEMENTMAP_PROP_X_CHANNEL_SELECT, D2D1_DISPLACEMENTMAP_PROP_Y_CHANNEL_SELECT, d2d1effects/D2D1_DISPLACEMENTMAP_PROP, d2d1effects/D2D1_DISPLACEMENTMAP_PROP_SCALE, d2d1effects/D2D1_DISPLACEMENTMAP_PROP_X_CHANNEL_SELECT, d2d1effects/D2D1_DISPLACEMENTMAP_PROP_Y_CHANNEL_SELECT, direct2d.d2d1_displacementmap_prop
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
 - D2D1_DISPLACEMENTMAP_PROP
product: Windows
targetos: Windows
req.typenames: D2D1_DISPLACEMENTMAP_PROP
req.redist: 
---

# D2D1_DISPLACEMENTMAP_PROP enumeration


## -description


Identifiers for properties of the <a href="https://msdn.microsoft.com/07AA64B1-B570-428E-924F-D7DF3E4DB3F8">Displacement map effect</a>.
        


## -enum-fields




### -field D2D1_DISPLACEMENTMAP_PROP_SCALE

Multiplies the intensity of the selected channel from the displacement image. The higher you set this property, the more the effect displaces the pixels.
            

The type is FLOAT.

The default value is 0.0f.


### -field D2D1_DISPLACEMENTMAP_PROP_X_CHANNEL_SELECT

The effect extracts the intensity from this color channel and uses it to spatially displace the image in the X direction.
          

The type is <a href="https://msdn.microsoft.com/92BC07F7-4CB5-487E-9AFB-255C8EF1C6BA">D2D1_CHANNEL_SELECTOR</a>.

The default value is D2D1_CHANNEL_SELECTOR_A


### -field D2D1_DISPLACEMENTMAP_PROP_Y_CHANNEL_SELECT

The effect extracts the intensity from this color channel and uses it to spatially displace the image in the Y direction.
          

The type is <a href="https://msdn.microsoft.com/92BC07F7-4CB5-487E-9AFB-255C8EF1C6BA">D2D1_CHANNEL_SELECTOR</a>.

The default value is D2D1_CHANNEL_SELECTOR_A


### -field D2D1_DISPLACEMENTMAP_PROP_FORCE_DWORD



