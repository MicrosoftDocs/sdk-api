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

# D2D1_3DPERSPECTIVETRANSFORM_PROP enumeration


## -description



          Identifiers for the properties of the <a href="https://msdn.microsoft.com/0E1A940E-2DCA-4772-BB68-7E5EF5CEF833">3D perspective transform effect</a>.
        


## -enum-fields




### -field D2D1_3DPERSPECTIVETRANSFORM_PROP_INTERPOLATION_MODE


            The interpolation mode the effect uses on the image. There are 5 scale modes that range in quality and speed.
            

Type is D2D1_3DPERSPECTIVETRANSFORM_INTERPOLATION_MODE.

Default value is D2D1_3DPERSPECTIVETRANSFORM_INTERPOLATION_MODE_LINEAR.


### -field D2D1_3DPERSPECTIVETRANSFORM_PROP_BORDER_MODE


            The mode used to calculate the border of the image, soft or hard. See Border modes for more info.
            

Type is D2D1_BORDER_MODE.

Default value is D2D1_BORDER_MODE_SOFT.


### -field D2D1_3DPERSPECTIVETRANSFORM_PROP_DEPTH


            The distance from the PerspectiveOrigin to the projection plane. The value specified in DIPs and must be greater than 0.
            

Type is FLOAT.

Default value is 1000.0f.


### -field D2D1_3DPERSPECTIVETRANSFORM_PROP_PERSPECTIVE_ORIGIN


            The X and Y location of the viewer in the 3D scene. This property is a D2D1_VECTOR_2F defined as: (point X, point Y). The units are in DIPs.
            You set the Z value with the Depth property.
            

Type is D2D1_VECTOR_2F.

Default value is {0.0f, 0.0f}.


### -field D2D1_3DPERSPECTIVETRANSFORM_PROP_LOCAL_OFFSET


            A translation the effect performs before it rotates the projection plane. This property is a D2D1_VECTOR_3F defined as: (X, Y, Z). The units are in DIPs.
            

Type is D2D1_VECTOR_3F.

Default value is {0.0f, 0.0f, 0.0f}.


### -field D2D1_3DPERSPECTIVETRANSFORM_PROP_GLOBAL_OFFSET


            A translation the effect performs after it rotates the projection plane. This property is a D2D1_VECTOR_3F defined as: (X, Y, Z). The units are in DIPs.
            

Type is D2D1_VECTOR_3F.

Default value is {0.0f, 0.0f, 0.0f}.


### -field D2D1_3DPERSPECTIVETRANSFORM_PROP_ROTATION_ORIGIN


            The center point of the rotation the effect performs. This property is a D2D1_VECTOR_3F defined as: (X, Y, Z). The units are in DIPs.
            

Type is D2D1_VECTOR_3F.

Default value is {0.0f, 0.0f, 0.0f}.


### -field D2D1_3DPERSPECTIVETRANSFORM_PROP_ROTATION


            The angles of rotation for each axis. This property is a D2D1_VECTOR_3F defined as: (X, Y, Z). The units are in degrees.
            

Type is D2D1_VECTOR_3F.

Default value is {0.0f, 0.0f, 0.0f}.


### -field D2D1_3DPERSPECTIVETRANSFORM_PROP_FORCE_DWORD



