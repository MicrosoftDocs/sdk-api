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

# D2D1_3DTRANSFORM_PROP enumeration


## -description



          Identifiers for properties of the <a href="https://msdn.microsoft.com/BC2F2837-40F0-4293-A190-8B5F81BB01B6">3D transform effect</a>.
        


## -enum-fields




### -field D2D1_3DTRANSFORM_PROP_INTERPOLATION_MODE


            The interpolation mode the effect uses on the image. There are 5 scale modes that range in quality and speed.
            

Type is D2D1_3DTRANSFORM_INTERPOLATION_MODE.

Default value is D2D1_3DTRANSFORM_INTERPOLATION_MODE_LINEAR.


### -field D2D1_3DTRANSFORM_PROP_BORDER_MODE


            The mode used to calculate the border of the image, soft or hard. See Border modes for more info.
            

Type is D2D1_BORDER_MODE.

Default value is D2D1_BORDER_MODE_SOFT.


### -field D2D1_3DTRANSFORM_PROP_TRANSFORM_MATRIX


              A 4x4 transform matrix applied to the projection plane. The following matrix calculation is used to map points from one 3D coordinate system
              to the transformed 2D coordinate system.
            

<img alt="3D Depth Matrix" src="images/3d_transform_matrix1.png"/>

              Where:<dl>
<dd>X, Y, Z = Input projection plane coordinates</dd>
<dd>
                  M<sub>x,y</sub> = Transform Matrix elements
                </dd>
<dd>X’, Y’, Z’ =Output projection plane coordinates</dd>
</dl>


The individual matrix elements are not bounded and are unitless. 

Type is D2D1_MATRIX_4X4_F.


              Default value is Matrix4x4F(1, 0, 0, 0,
              0, 1, 0, 0,
              0, 0, 1, 0,
              0, 0, 0, 1).
            


### -field D2D1_3DTRANSFORM_PROP_FORCE_DWORD



