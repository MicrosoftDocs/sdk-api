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



