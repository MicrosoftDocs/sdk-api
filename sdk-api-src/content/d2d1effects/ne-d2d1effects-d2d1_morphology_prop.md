---
UID: NE:d2d1effects.D2D1_MORPHOLOGY_PROP
title: D2D1_MORPHOLOGY_PROP
author: windows-sdk-content
description: Identifiers for properties of the Morphology effect.
old-location: direct2d\d2d1_morphology_prop.htm
tech.root: direct2d
ms.assetid: D5916AD4-F19A-42F0-BA24-B61BA9786013
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D2D1_MORPHOLOGY_PROP, D2D1_MORPHOLOGY_PROP enumeration [Direct2D], D2D1_MORPHOLOGY_PROP_HEIGHT, D2D1_MORPHOLOGY_PROP_MODE, D2D1_MORPHOLOGY_PROP_WIDTH, d2d1effects/D2D1_MORPHOLOGY_PROP, d2d1effects/D2D1_MORPHOLOGY_PROP_HEIGHT, d2d1effects/D2D1_MORPHOLOGY_PROP_MODE, d2d1effects/D2D1_MORPHOLOGY_PROP_WIDTH, direct2d.d2d1_morphology_prop
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - D2D1_MORPHOLOGY_PROP
product: Windows
targetos: Windows
req.typenames: D2D1_MORPHOLOGY_PROP
req.redist: 
---

# D2D1_MORPHOLOGY_PROP enumeration


## -description


Identifiers for properties of the <a href="https://msdn.microsoft.com/en-us/library/Hh706364(v=VS.85).aspx">Morphology effect</a>.
        


## -enum-fields




### -field D2D1_MORPHOLOGY_PROP_MODE

The morphology mode.
            

The type is D2D1_MORPHOLOGY_MODE.

The default value is D2D1_MORPHOLOGY_MODE_ERODE.


### -field D2D1_MORPHOLOGY_PROP_WIDTH

Size of the kernel in the X direction. The units are in DIPs. Values must be between 1 and 100 inclusive.
            

The type is UINT.

The default value is 1.


### -field D2D1_MORPHOLOGY_PROP_HEIGHT

Size of the kernel in the Y direction. The units are in DIPs. Values must be between 1 and 100 inclusive.
            

The type is UINT.

The default value is 1.


### -field D2D1_MORPHOLOGY_PROP_FORCE_DWORD



