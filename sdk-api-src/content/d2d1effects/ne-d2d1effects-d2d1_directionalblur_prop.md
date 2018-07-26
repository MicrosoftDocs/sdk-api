---
UID: NE:d2d1effects.D2D1_DIRECTIONALBLUR_PROP
title: D2D1_DIRECTIONALBLUR_PROP
author: windows-sdk-content
description: Identifiers for properties of the Directional blur effect.
old-location: direct2d\d2d1_directionalblur_prop.htm
old-project: Direct2D
ms.assetid: BEC82079-543E-4675-84DD-0DE7D852866E
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: D2D1_DIRECTIONALBLUR_PROP, D2D1_DIRECTIONALBLUR_PROP enumeration [Direct2D], D2D1_DIRECTIONALBLUR_PROP_ANGLE, D2D1_DIRECTIONALBLUR_PROP_BORDER_MODE, D2D1_DIRECTIONALBLUR_PROP_OPTIMIZATION, D2D1_DIRECTIONALBLUR_PROP_STANDARD_DEVIATION, d2d1effects/D2D1_DIRECTIONALBLUR_PROP, d2d1effects/D2D1_DIRECTIONALBLUR_PROP_ANGLE, d2d1effects/D2D1_DIRECTIONALBLUR_PROP_BORDER_MODE, d2d1effects/D2D1_DIRECTIONALBLUR_PROP_OPTIMIZATION, d2d1effects/D2D1_DIRECTIONALBLUR_PROP_STANDARD_DEVIATION, direct2d.d2d1_directionalblur_prop
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
tech.root: 
req.typenames: D2D1_DIRECTIONALBLUR_PROP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1effects.h
api_name:
 - D2D1_DIRECTIONALBLUR_PROP
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
---

# D2D1_DIRECTIONALBLUR_PROP enumeration


## -description


Identifiers for properties of the <a href="https://msdn.microsoft.com/59328FA4-5C27-4A81-AAB2-C5B25B3615C6">Directional blur effect</a>.
        


## -enum-fields




### -field D2D1_DIRECTIONALBLUR_PROP_STANDARD_DEVIATION

The amount of blur to be applied to the image. You can compute the blur radius of the kernel by multiplying the standard deviation by 3. 
          The units of both the standard deviation and blur radius are DIPs. A value of 0 DIPs disables this effect. 
          

The type is FLOAT.

The default value is 3.0f.


### -field D2D1_DIRECTIONALBLUR_PROP_ANGLE

The angle of the blur relative to the x-axis, in the counterclockwise direction. The units are specified in degrees.
          

The blur kernel is first generated using the same process as for the Gaussian blur effect. The kernel values are then transformed according to the blur angle.

The type is FLOAT.

The default value is 0.0f.


### -field D2D1_DIRECTIONALBLUR_PROP_OPTIMIZATION

The optimization mode. See Optimization modes for more info.
          

The type is <a href="https://msdn.microsoft.com/28B99069-3380-4D44-82A1-9A8F551B3C45">D2D1_DIRECTIONALBLUR_OPTIMIZATION</a>.

The default value is D2D1_DIRECTIONALBLUR_OPTIMIZATION_BALANCED. 


### -field D2D1_DIRECTIONALBLUR_PROP_BORDER_MODE

The mode used to calculate the border of the image, soft or hard. See Border modes for more info.
          

The type is <a href="https://msdn.microsoft.com/093C7028-9C0E-4BB5-9769-C456B7A23B6F">D2D1_BORDER_MODE</a>.

The default value is D2D1_BORDER_MODE_SOFT.


### -field D2D1_DIRECTIONALBLUR_PROP_FORCE_DWORD



