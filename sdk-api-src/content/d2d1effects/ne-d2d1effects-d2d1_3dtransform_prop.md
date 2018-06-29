---
UID: NE:d2d1effects.D2D1_3DTRANSFORM_PROP
title: D2D1_3DTRANSFORM_PROP
author: windows-sdk-content
description: Identifiers for properties of the 3D transform effect.
old-location: direct2d\d2d1_3dtransform_prop.htm
old-project: Direct2D
ms.assetid: 56004ED1-66E2-44ED-B274-E7FF8C641954
ms.author: windowssdkdev
ms.date: 04/20/2018
ms.keywords: D2D1_3DTRANSFORM_PROP, D2D1_3DTRANSFORM_PROP enumeration [Direct2D], D2D1_3DTRANSFORM_PROP_BORDER_MODE, D2D1_3DTRANSFORM_PROP_INTERPOLATION_MODE, D2D1_3DTRANSFORM_PROP_TRANSFORM_MATRIX, d2d1effects/D2D1_3DTRANSFORM_PROP, d2d1effects/D2D1_3DTRANSFORM_PROP_BORDER_MODE, d2d1effects/D2D1_3DTRANSFORM_PROP_INTERPOLATION_MODE, d2d1effects/D2D1_3DTRANSFORM_PROP_TRANSFORM_MATRIX, direct2d.d2d1_3dtransform_prop
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
req.typenames: D2D1_3DTRANSFORM_PROP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1effects.h
api_name:
 - D2D1_3DTRANSFORM_PROP
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
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
            

<img alt="3D Depth Matrix" src="./images/3d_transform_matrix1.png"/>

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



