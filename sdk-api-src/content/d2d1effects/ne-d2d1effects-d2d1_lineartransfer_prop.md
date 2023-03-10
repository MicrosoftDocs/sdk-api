---
UID: NE:d2d1effects.D2D1_LINEARTRANSFER_PROP
title: D2D1_LINEARTRANSFER_PROP (d2d1effects.h)
description: Identifiers for properties of the Linear transfer effect.
helpviewer_keywords: ["D2D1_LINEARTRANSFER_PROP","D2D1_LINEARTRANSFER_PROP enumeration [Direct2D]","D2D1_LINEARTRANSFER_PROP_ALPHA_DISABLE","D2D1_LINEARTRANSFER_PROP_ALPHA_SLOPE","D2D1_LINEARTRANSFER_PROP_ALPHA_Y_INTERCEPT","D2D1_LINEARTRANSFER_PROP_BLUE_DISABLE","D2D1_LINEARTRANSFER_PROP_BLUE_SLOPE","D2D1_LINEARTRANSFER_PROP_BLUE_Y_INTERCEPT","D2D1_LINEARTRANSFER_PROP_CLAMP_OUTPUT","D2D1_LINEARTRANSFER_PROP_GREEN_DISABLE","D2D1_LINEARTRANSFER_PROP_GREEN_SLOPE","D2D1_LINEARTRANSFER_PROP_GREEN_Y_INTERCEPT","D2D1_LINEARTRANSFER_PROP_RED_DISABLE","D2D1_LINEARTRANSFER_PROP_RED_SLOPE","D2D1_LINEARTRANSFER_PROP_RED_Y_INTERCEPT","d2d1effects/D2D1_LINEARTRANSFER_PROP","d2d1effects/D2D1_LINEARTRANSFER_PROP_ALPHA_DISABLE","d2d1effects/D2D1_LINEARTRANSFER_PROP_ALPHA_SLOPE","d2d1effects/D2D1_LINEARTRANSFER_PROP_ALPHA_Y_INTERCEPT","d2d1effects/D2D1_LINEARTRANSFER_PROP_BLUE_DISABLE","d2d1effects/D2D1_LINEARTRANSFER_PROP_BLUE_SLOPE","d2d1effects/D2D1_LINEARTRANSFER_PROP_BLUE_Y_INTERCEPT","d2d1effects/D2D1_LINEARTRANSFER_PROP_CLAMP_OUTPUT","d2d1effects/D2D1_LINEARTRANSFER_PROP_GREEN_DISABLE","d2d1effects/D2D1_LINEARTRANSFER_PROP_GREEN_SLOPE","d2d1effects/D2D1_LINEARTRANSFER_PROP_GREEN_Y_INTERCEPT","d2d1effects/D2D1_LINEARTRANSFER_PROP_RED_DISABLE","d2d1effects/D2D1_LINEARTRANSFER_PROP_RED_SLOPE","d2d1effects/D2D1_LINEARTRANSFER_PROP_RED_Y_INTERCEPT","direct2d.d2d1_lineartransfer_prop"]
old-location: direct2d\d2d1_lineartransfer_prop.htm
tech.root: Direct2D
ms.assetid: 25D06C2C-210F-4C10-9842-4355C9371902
ms.date: 12/05/2018
ms.keywords: D2D1_LINEARTRANSFER_PROP, D2D1_LINEARTRANSFER_PROP enumeration [Direct2D], D2D1_LINEARTRANSFER_PROP_ALPHA_DISABLE, D2D1_LINEARTRANSFER_PROP_ALPHA_SLOPE, D2D1_LINEARTRANSFER_PROP_ALPHA_Y_INTERCEPT, D2D1_LINEARTRANSFER_PROP_BLUE_DISABLE, D2D1_LINEARTRANSFER_PROP_BLUE_SLOPE, D2D1_LINEARTRANSFER_PROP_BLUE_Y_INTERCEPT, D2D1_LINEARTRANSFER_PROP_CLAMP_OUTPUT, D2D1_LINEARTRANSFER_PROP_GREEN_DISABLE, D2D1_LINEARTRANSFER_PROP_GREEN_SLOPE, D2D1_LINEARTRANSFER_PROP_GREEN_Y_INTERCEPT, D2D1_LINEARTRANSFER_PROP_RED_DISABLE, D2D1_LINEARTRANSFER_PROP_RED_SLOPE, D2D1_LINEARTRANSFER_PROP_RED_Y_INTERCEPT, d2d1effects/D2D1_LINEARTRANSFER_PROP, d2d1effects/D2D1_LINEARTRANSFER_PROP_ALPHA_DISABLE, d2d1effects/D2D1_LINEARTRANSFER_PROP_ALPHA_SLOPE, d2d1effects/D2D1_LINEARTRANSFER_PROP_ALPHA_Y_INTERCEPT, d2d1effects/D2D1_LINEARTRANSFER_PROP_BLUE_DISABLE, d2d1effects/D2D1_LINEARTRANSFER_PROP_BLUE_SLOPE, d2d1effects/D2D1_LINEARTRANSFER_PROP_BLUE_Y_INTERCEPT, d2d1effects/D2D1_LINEARTRANSFER_PROP_CLAMP_OUTPUT, d2d1effects/D2D1_LINEARTRANSFER_PROP_GREEN_DISABLE, d2d1effects/D2D1_LINEARTRANSFER_PROP_GREEN_SLOPE, d2d1effects/D2D1_LINEARTRANSFER_PROP_GREEN_Y_INTERCEPT, d2d1effects/D2D1_LINEARTRANSFER_PROP_RED_DISABLE, d2d1effects/D2D1_LINEARTRANSFER_PROP_RED_SLOPE, d2d1effects/D2D1_LINEARTRANSFER_PROP_RED_Y_INTERCEPT, direct2d.d2d1_lineartransfer_prop
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
req.typenames: D2D1_LINEARTRANSFER_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_LINEARTRANSFER_PROP
 - d2d1effects/D2D1_LINEARTRANSFER_PROP
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
 - D2D1_LINEARTRANSFER_PROP
---

# D2D1_LINEARTRANSFER_PROP enumeration


## -description

Identifiers for properties of the <a href="/windows/desktop/Direct2D/linear-transfer">Linear transfer effect</a>.

## -enum-fields

### -field D2D1_LINEARTRANSFER_PROP_RED_Y_INTERCEPT:0

The Y-intercept of the linear function for the Red channel. 
          

The type is FLOAT.

The default is 0.0f.

### -field D2D1_LINEARTRANSFER_PROP_RED_SLOPE:1

The slope of the linear function for the Red channel.
          

The type is FLOAT.

The default is 1.0f.

### -field D2D1_LINEARTRANSFER_PROP_RED_DISABLE:2

If you set this to TRUE the effect does not apply the transfer function to the Red channel. 
          If you set this to FALSE the effect applies the RedLinearTransfer function to the Red channel. 
          

The type is BOOL.

The default is FALSE.

### -field D2D1_LINEARTRANSFER_PROP_GREEN_Y_INTERCEPT:3

The Y-intercept of the linear function for the Green channel. 
          

The type is FLOAT.

The default is 0.0f.

### -field D2D1_LINEARTRANSFER_PROP_GREEN_SLOPE:4

The slope of the linear function for the Green channel.
          

The type is FLOAT.

The default is 1.0f.

### -field D2D1_LINEARTRANSFER_PROP_GREEN_DISABLE:5

If you set this to TRUE the effect does not apply the transfer function to the Green channel. 
          If you set this to FALSE the effect applies the GreenLinearTransfer function to the Green channel. 
          

The type is BOOL.

The default is FALSE.

### -field D2D1_LINEARTRANSFER_PROP_BLUE_Y_INTERCEPT:6

The Y-intercept of the linear function for the Blue channel. 
          

The type is FLOAT.

The default is 0.0f.

### -field D2D1_LINEARTRANSFER_PROP_BLUE_SLOPE:7

The slope of the linear function for the Blue channel.
          

The type is FLOAT.

The default is 1.0f.

### -field D2D1_LINEARTRANSFER_PROP_BLUE_DISABLE:8

If you set this to TRUE the effect does not apply the transfer function to the Blue channel. 
          If you set this to FALSE the effect applies the BlueLinearTransfer function to the Blue channel. 
          

The type is BOOL.

The default is FALSE.

### -field D2D1_LINEARTRANSFER_PROP_ALPHA_Y_INTERCEPT:9

The Y-intercept of the linear function for the Alpha channel. 
          

The type is FLOAT.

The default is 0.0f.

### -field D2D1_LINEARTRANSFER_PROP_ALPHA_SLOPE:10

The slope of the linear function for the Alpha channel.
          

The type is FLOAT.

The default is 0.0f.

### -field D2D1_LINEARTRANSFER_PROP_ALPHA_DISABLE:11

If you set this to TRUE the effect does not apply the transfer function to the Alpha channel. 
          If you set this to FALSE the effect applies the AlphaLinearTransfer function to the Alpha channel. 
          

The type is BOOL.

The default is FALSE.

### -field D2D1_LINEARTRANSFER_PROP_CLAMP_OUTPUT:12

Whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph. 
          The effect clamps the values before it premultiplies the alpha .
          

If you set this to TRUE the effect will clamp the values. If you set this to FALSE, the effect will not clamp the color values, but other effects and 
          the output surface may clamp the values if they are not of high enough precision.

The type is BOOL.

The default is FALSE.

### -field D2D1_LINEARTRANSFER_PROP_FORCE_DWORD:0xffffffff
