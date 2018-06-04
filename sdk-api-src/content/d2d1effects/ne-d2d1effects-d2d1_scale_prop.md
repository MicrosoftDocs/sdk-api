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

# D2D1_SCALE_PROP enumeration


## -description



          Identifiers for properties of the <a href="https://msdn.microsoft.com/99DFA8DB-384B-4F64-90A2-0D3D7E1ACF27">Scale effect</a>.
        


## -enum-fields




### -field D2D1_SCALE_PROP_SCALE


            The scale amount in the X and Y direction as a ratio of the output size to the input size.
            

This property a <a href="https://msdn.microsoft.com/DD180090-D2F4-4DF3-8652-101713C01AE4">D2D1_VECTOR_2F</a> defined as: (X scale, Y scale). 
            The scale amounts are FLOAT, unitless, and must be positive or 0.

The type is <a href="https://msdn.microsoft.com/DD180090-D2F4-4DF3-8652-101713C01AE4">D2D1_VECTOR_2F</a>.

The default value is {1.0f, 1.0f}.


### -field D2D1_SCALE_PROP_CENTER_POINT


            The image scaling center point. This property is a <a href="https://msdn.microsoft.com/DD180090-D2F4-4DF3-8652-101713C01AE4">D2D1_VECTOR_2F</a> defined as: (point X, point Y). The units are in DIPs.
            

Use the center point property to scale around a point other than the upper-left corner.

The type is <a href="https://msdn.microsoft.com/DD180090-D2F4-4DF3-8652-101713C01AE4">D2D1_VECTOR_2F</a>.

The default value is {0.0f, 0.0f}.


### -field D2D1_SCALE_PROP_INTERPOLATION_MODE


            The interpolation mode the effect uses to scale the image. There are 6 scale modes that range in quality and speed.
            

The type is <a href="https://msdn.microsoft.com/2673E6AE-EEF5-4727-B224-0245CED15C21">D2D1_SCALE_INTERPOLATION_MODE</a>.

The default value is D2D1_SCALE_INTERPOLATION_MODE_LINEAR.


### -field D2D1_SCALE_PROP_BORDER_MODE


            The mode used to calculate the border of the image, soft or hard. 
            

The type is <a href="https://msdn.microsoft.com/093C7028-9C0E-4BB5-9769-C456B7A23B6F">D2D1_BORDER_MODE</a>.

The default value is D2D1_BORDER_MODE_SOFT.


### -field D2D1_SCALE_PROP_SHARPNESS


            In the high quality cubic interpolation mode, the sharpness level of the scaling filter as a float between 0 and 1. The values are unitless. 
            You can use sharpness to adjust the quality of an image when you scale the image down.
            

The sharpness factor affects the shape of the kernel. The higher the sharpness factor, the smaller the kernel.

<div class="alert"><b>Note</b>  This property affects only the high quality cubic interpolation mode.</div>
<div> </div>
The type is FLOAT.

The default value is 0.0f.


### -field D2D1_SCALE_PROP_FORCE_DWORD



