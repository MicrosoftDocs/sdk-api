---
UID: NE:d2d1effects.D2D1_3DPERSPECTIVETRANSFORM_PROP
title: D2D1_3DPERSPECTIVETRANSFORM_PROP (d2d1effects.h)
description: Identifiers for the properties of the 3D perspective transform effect.
helpviewer_keywords: ["D2D1_3DPERSPECTIVETRANSFORM_PROP","D2D1_3DPERSPECTIVETRANSFORM_PROP enumeration [Direct2D]","D2D1_3DPERSPECTIVETRANSFORM_PROP_BORDER_MODE","D2D1_3DPERSPECTIVETRANSFORM_PROP_DEPTH","D2D1_3DPERSPECTIVETRANSFORM_PROP_GLOBAL_OFFSET","D2D1_3DPERSPECTIVETRANSFORM_PROP_INTERPOLATION_MODE","D2D1_3DPERSPECTIVETRANSFORM_PROP_LOCAL_OFFSET","D2D1_3DPERSPECTIVETRANSFORM_PROP_PERSPECTIVE_ORIGIN","D2D1_3DPERSPECTIVETRANSFORM_PROP_ROTATION","D2D1_3DPERSPECTIVETRANSFORM_PROP_ROTATION_ORIGIN","d2d1effects/D2D1_3DPERSPECTIVETRANSFORM_PROP","d2d1effects/D2D1_3DPERSPECTIVETRANSFORM_PROP_BORDER_MODE","d2d1effects/D2D1_3DPERSPECTIVETRANSFORM_PROP_DEPTH","d2d1effects/D2D1_3DPERSPECTIVETRANSFORM_PROP_GLOBAL_OFFSET","d2d1effects/D2D1_3DPERSPECTIVETRANSFORM_PROP_INTERPOLATION_MODE","d2d1effects/D2D1_3DPERSPECTIVETRANSFORM_PROP_LOCAL_OFFSET","d2d1effects/D2D1_3DPERSPECTIVETRANSFORM_PROP_PERSPECTIVE_ORIGIN","d2d1effects/D2D1_3DPERSPECTIVETRANSFORM_PROP_ROTATION","d2d1effects/D2D1_3DPERSPECTIVETRANSFORM_PROP_ROTATION_ORIGIN","direct2d.d2d1_3dperspectivetransform_prop"]
old-location: direct2d\d2d1_3dperspectivetransform_prop.htm
tech.root: Direct2D
ms.assetid: 12CD4038-7907-4E0E-8751-00E32EBA2A77
ms.date: 12/05/2018
ms.keywords: D2D1_3DPERSPECTIVETRANSFORM_PROP, D2D1_3DPERSPECTIVETRANSFORM_PROP enumeration [Direct2D], D2D1_3DPERSPECTIVETRANSFORM_PROP_BORDER_MODE, D2D1_3DPERSPECTIVETRANSFORM_PROP_DEPTH, D2D1_3DPERSPECTIVETRANSFORM_PROP_GLOBAL_OFFSET, D2D1_3DPERSPECTIVETRANSFORM_PROP_INTERPOLATION_MODE, D2D1_3DPERSPECTIVETRANSFORM_PROP_LOCAL_OFFSET, D2D1_3DPERSPECTIVETRANSFORM_PROP_PERSPECTIVE_ORIGIN, D2D1_3DPERSPECTIVETRANSFORM_PROP_ROTATION, D2D1_3DPERSPECTIVETRANSFORM_PROP_ROTATION_ORIGIN, d2d1effects/D2D1_3DPERSPECTIVETRANSFORM_PROP, d2d1effects/D2D1_3DPERSPECTIVETRANSFORM_PROP_BORDER_MODE, d2d1effects/D2D1_3DPERSPECTIVETRANSFORM_PROP_DEPTH, d2d1effects/D2D1_3DPERSPECTIVETRANSFORM_PROP_GLOBAL_OFFSET, d2d1effects/D2D1_3DPERSPECTIVETRANSFORM_PROP_INTERPOLATION_MODE, d2d1effects/D2D1_3DPERSPECTIVETRANSFORM_PROP_LOCAL_OFFSET, d2d1effects/D2D1_3DPERSPECTIVETRANSFORM_PROP_PERSPECTIVE_ORIGIN, d2d1effects/D2D1_3DPERSPECTIVETRANSFORM_PROP_ROTATION, d2d1effects/D2D1_3DPERSPECTIVETRANSFORM_PROP_ROTATION_ORIGIN, direct2d.d2d1_3dperspectivetransform_prop
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
targetos: Windows
req.typenames: D2D1_3DPERSPECTIVETRANSFORM_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_3DPERSPECTIVETRANSFORM_PROP
 - d2d1effects/D2D1_3DPERSPECTIVETRANSFORM_PROP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1effects.h
api_name:
 - D2D1_3DPERSPECTIVETRANSFORM_PROP
---

# D2D1_3DPERSPECTIVETRANSFORM_PROP enumeration


## -description

Identifiers for the properties of the <a href="/windows/desktop/Direct2D/3d-perspective-transform">3D perspective transform effect</a>.

## -enum-fields

### -field D2D1_3DPERSPECTIVETRANSFORM_PROP_INTERPOLATION_MODE:0

The interpolation mode the effect uses on the image. There are 5 scale modes that range in quality and speed.
            

Type is D2D1_3DPERSPECTIVETRANSFORM_INTERPOLATION_MODE.

Default value is D2D1_3DPERSPECTIVETRANSFORM_INTERPOLATION_MODE_LINEAR.

### -field D2D1_3DPERSPECTIVETRANSFORM_PROP_BORDER_MODE:1

The mode used to calculate the border of the image, soft or hard. See Border modes for more info.
            

Type is D2D1_BORDER_MODE.

Default value is D2D1_BORDER_MODE_SOFT.

### -field D2D1_3DPERSPECTIVETRANSFORM_PROP_DEPTH:2

The distance from the PerspectiveOrigin to the projection plane. The value specified in DIPs and must be greater than 0.
            

Type is FLOAT.

Default value is 1000.0f.

### -field D2D1_3DPERSPECTIVETRANSFORM_PROP_PERSPECTIVE_ORIGIN:3

The X and Y location of the viewer in the 3D scene. This property is a D2D1_VECTOR_2F defined as: (point X, point Y). The units are in DIPs.
            You set the Z value with the Depth property.
            

Type is D2D1_VECTOR_2F.

Default value is {0.0f, 0.0f}.

### -field D2D1_3DPERSPECTIVETRANSFORM_PROP_LOCAL_OFFSET:4

A translation the effect performs before it rotates the projection plane. This property is a D2D1_VECTOR_3F defined as: (X, Y, Z). The units are in DIPs.
            

Type is D2D1_VECTOR_3F.

Default value is {0.0f, 0.0f, 0.0f}.

### -field D2D1_3DPERSPECTIVETRANSFORM_PROP_GLOBAL_OFFSET:5

A translation the effect performs after it rotates the projection plane. This property is a D2D1_VECTOR_3F defined as: (X, Y, Z). The units are in DIPs.
            

Type is D2D1_VECTOR_3F.

Default value is {0.0f, 0.0f, 0.0f}.

### -field D2D1_3DPERSPECTIVETRANSFORM_PROP_ROTATION_ORIGIN:6

The center point of the rotation the effect performs. This property is a D2D1_VECTOR_3F defined as: (X, Y, Z). The units are in DIPs.
            

Type is D2D1_VECTOR_3F.

Default value is {0.0f, 0.0f, 0.0f}.

### -field D2D1_3DPERSPECTIVETRANSFORM_PROP_ROTATION:7

The angles of rotation for each axis. This property is a D2D1_VECTOR_3F defined as: (X, Y, Z). The units are in degrees.
            

Type is D2D1_VECTOR_3F.

Default value is {0.0f, 0.0f, 0.0f}.

### -field D2D1_3DPERSPECTIVETRANSFORM_PROP_FORCE_DWORD:0xffffffff
