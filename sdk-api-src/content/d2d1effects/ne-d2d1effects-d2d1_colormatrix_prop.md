---
UID: NE:d2d1effects.D2D1_COLORMATRIX_PROP
title: D2D1_COLORMATRIX_PROP
author: windows-sdk-content
description: Identifiers for the properties of the Color matrix effect.
old-location: direct2d\d2d1_colormatrix_prop.htm
old-project: direct2d
ms.assetid: 7A171DAF-08E4-46FF-9FAF-54A83E805555
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: D2D1_COLORMATRIX_PROP, D2D1_COLORMATRIX_PROP enumeration [Direct2D], D2D1_COLORMATRIX_PROP_ALPHA_MODE, D2D1_COLORMATRIX_PROP_CLAMP_OUTPUT, D2D1_COLORMATRIX_PROP_COLOR_MATRIX, d2d1effects/D2D1_COLORMATRIX_PROP, d2d1effects/D2D1_COLORMATRIX_PROP_ALPHA_MODE, d2d1effects/D2D1_COLORMATRIX_PROP_CLAMP_OUTPUT, d2d1effects/D2D1_COLORMATRIX_PROP_COLOR_MATRIX, direct2d.d2d1_colormatrix_prop
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d2d1effects.h
req.include-header: 
req.redist: 
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
req.typenames: D2D1_COLORMATRIX_PROP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1effects.h
api_name:
 - D2D1_COLORMATRIX_PROP
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
---

# D2D1_COLORMATRIX_PROP enumeration


## -description


Identifiers for the properties of the <a href="https://msdn.microsoft.com/en-us/library/Hh706319(v=VS.85).aspx">Color matrix effect</a>.


## -enum-fields




### -field D2D1_COLORMATRIX_PROP_COLOR_MATRIX

A 5x4 matrix of float values. The elements in the matrix are not bounded and are unitless.
          

The type is <a href="https://msdn.microsoft.com/en-us/library/Dn958413(v=VS.85).aspx">D2D1_MATRIX_5X4_F</a>.

The default value is the identity matrix, Matrix5x4F(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0).


### -field D2D1_COLORMATRIX_PROP_ALPHA_MODE

The alpha mode of the output. 
          

The type is <a href="https://msdn.microsoft.com/en-us/library/Dn934229(v=VS.85).aspx">D2D1_COLORMATRIX_ALPHA_MODE</a>.

The default value is D2D1_COLORMATRIX_ALPHA_MODE_PREMULTIPLIED.


### -field D2D1_COLORMATRIX_PROP_CLAMP_OUTPUT

Whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph. 
          The effect clamps the values before it premultiplies the alpha.
          

If you set this to TRUE the effect will clamp the values. If you set this to FALSE, the effect will not clamp the color values, 
          but other effects and the output surface may clamp the values if they are not of high enough precision.

The type is BOOL.

The default value is FALSE.


### -field D2D1_COLORMATRIX_PROP_FORCE_DWORD



