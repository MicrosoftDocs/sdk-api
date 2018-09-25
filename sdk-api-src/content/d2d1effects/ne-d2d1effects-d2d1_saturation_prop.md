---
UID: NE:d2d1effects.D2D1_SATURATION_PROP
title: D2D1_SATURATION_PROP
author: windows-sdk-content
description: Identifiers for properties of the Saturation effect.
old-location: direct2d\d2d1_saturation_prop.htm
tech.root: direct2d
ms.assetid: 69F237FD-F9EE-4C6B-B6E1-673FE815FC6D
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: D2D1_SATURATION_PROP, D2D1_SATURATION_PROP enumeration [Direct2D], D2D1_SATURATION_PROP_SATURATION, d2d1effects/D2D1_SATURATION_PROP, d2d1effects/D2D1_SATURATION_PROP_SATURATION, direct2d.d2d1_saturation_prop
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
 - D2D1_SATURATION_PROP
product: Windows
targetos: Windows
req.typenames: D2D1_SATURATION_PROP
req.redist: 
---

# D2D1_SATURATION_PROP enumeration


## -description


Identifiers for properties of the <a href="https://msdn.microsoft.com/03A374D9-BED4-49ED-B90E-21193909C8AB">Saturation effect</a>.


## -enum-fields




### -field D2D1_SATURATION_PROP_SATURATION

The saturation of the image. You can set the saturation to a value between 0 and 1. If you set it to 1 the output image is fully saturated. 
          If you set it to 0 the output image is monochrome. The saturation value is unitless.
          

The type is FLOAT.

The default is 0.5f.


### -field D2D1_SATURATION_PROP_FORCE_DWORD



