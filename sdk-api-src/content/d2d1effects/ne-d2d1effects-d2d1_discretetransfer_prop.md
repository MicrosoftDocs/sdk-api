---
UID: NE:d2d1effects.D2D1_DISCRETETRANSFER_PROP
title: D2D1_DISCRETETRANSFER_PROP (d2d1effects.h)
description: Identifiers for properties of the Discrete transfer effect.
helpviewer_keywords: ["D2D1_DISCRETETRANSFER_PROP","D2D1_DISCRETETRANSFER_PROP enumeration [Direct2D]","D2D1_DISCRETETRANSFER_PROP_ALPHA_DISABLE","D2D1_DISCRETETRANSFER_PROP_ALPHA_TABLE","D2D1_DISCRETETRANSFER_PROP_BLUE_DISABLE","D2D1_DISCRETETRANSFER_PROP_BLUE_TABLE","D2D1_DISCRETETRANSFER_PROP_CLAMP_OUTPUT","D2D1_DISCRETETRANSFER_PROP_GREEN_DISABLE","D2D1_DISCRETETRANSFER_PROP_GREEN_TABLE","D2D1_DISCRETETRANSFER_PROP_RED_DISABLE","D2D1_DISCRETETRANSFER_PROP_RED_TABLE","d2d1effects/D2D1_DISCRETETRANSFER_PROP","d2d1effects/D2D1_DISCRETETRANSFER_PROP_ALPHA_DISABLE","d2d1effects/D2D1_DISCRETETRANSFER_PROP_ALPHA_TABLE","d2d1effects/D2D1_DISCRETETRANSFER_PROP_BLUE_DISABLE","d2d1effects/D2D1_DISCRETETRANSFER_PROP_BLUE_TABLE","d2d1effects/D2D1_DISCRETETRANSFER_PROP_CLAMP_OUTPUT","d2d1effects/D2D1_DISCRETETRANSFER_PROP_GREEN_DISABLE","d2d1effects/D2D1_DISCRETETRANSFER_PROP_GREEN_TABLE","d2d1effects/D2D1_DISCRETETRANSFER_PROP_RED_DISABLE","d2d1effects/D2D1_DISCRETETRANSFER_PROP_RED_TABLE","direct2d.d2d1_discretetransfer_prop"]
old-location: direct2d\d2d1_discretetransfer_prop.htm
tech.root: Direct2D
ms.assetid: F00C9CF5-7103-450B-A211-02BB49A88EF8
ms.date: 12/05/2018
ms.keywords: D2D1_DISCRETETRANSFER_PROP, D2D1_DISCRETETRANSFER_PROP enumeration [Direct2D], D2D1_DISCRETETRANSFER_PROP_ALPHA_DISABLE, D2D1_DISCRETETRANSFER_PROP_ALPHA_TABLE, D2D1_DISCRETETRANSFER_PROP_BLUE_DISABLE, D2D1_DISCRETETRANSFER_PROP_BLUE_TABLE, D2D1_DISCRETETRANSFER_PROP_CLAMP_OUTPUT, D2D1_DISCRETETRANSFER_PROP_GREEN_DISABLE, D2D1_DISCRETETRANSFER_PROP_GREEN_TABLE, D2D1_DISCRETETRANSFER_PROP_RED_DISABLE, D2D1_DISCRETETRANSFER_PROP_RED_TABLE, d2d1effects/D2D1_DISCRETETRANSFER_PROP, d2d1effects/D2D1_DISCRETETRANSFER_PROP_ALPHA_DISABLE, d2d1effects/D2D1_DISCRETETRANSFER_PROP_ALPHA_TABLE, d2d1effects/D2D1_DISCRETETRANSFER_PROP_BLUE_DISABLE, d2d1effects/D2D1_DISCRETETRANSFER_PROP_BLUE_TABLE, d2d1effects/D2D1_DISCRETETRANSFER_PROP_CLAMP_OUTPUT, d2d1effects/D2D1_DISCRETETRANSFER_PROP_GREEN_DISABLE, d2d1effects/D2D1_DISCRETETRANSFER_PROP_GREEN_TABLE, d2d1effects/D2D1_DISCRETETRANSFER_PROP_RED_DISABLE, d2d1effects/D2D1_DISCRETETRANSFER_PROP_RED_TABLE, direct2d.d2d1_discretetransfer_prop
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
req.typenames: D2D1_DISCRETETRANSFER_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_DISCRETETRANSFER_PROP
 - d2d1effects/D2D1_DISCRETETRANSFER_PROP
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
 - D2D1_DISCRETETRANSFER_PROP
---

# D2D1_DISCRETETRANSFER_PROP enumeration


## -description

Identifiers for properties of the <a href="/windows/desktop/Direct2D/discrete-transfer">Discrete transfer effect</a>.

## -enum-fields

### -field D2D1_DISCRETETRANSFER_PROP_RED_TABLE:0

The list of values used to define the transfer function for the Red channel.
          

The type is FLOAT[].

The default value is {0.0f, 1.0f}.

### -field D2D1_DISCRETETRANSFER_PROP_RED_DISABLE:1

If you set this to TRUE the effect does not apply the transfer function to the Red channel. 
          If you set this to FALSE the effect applies the RedDiscreteTransfer function to the Red channel.
          

The type is BOOL.

The default value if FALSE.

### -field D2D1_DISCRETETRANSFER_PROP_GREEN_TABLE:2

The list of values used to define the transfer function for the Green channel.
          

The type is FLOAT[].

The default value is {0.0f, 1.0f}.

### -field D2D1_DISCRETETRANSFER_PROP_GREEN_DISABLE:3

If you set this to TRUE the effect does not apply the transfer function to the Green channel. 
          If you set this to FALSE the effect applies the GreenDiscreteTransfer function to the Green channel.
          

The type is BOOL.

The default value if FALSE.

### -field D2D1_DISCRETETRANSFER_PROP_BLUE_TABLE:4

The list of values used to define the transfer function for the Blue channel.
          

The type is FLOAT[].

The default value is {0.0f, 1.0f}.

### -field D2D1_DISCRETETRANSFER_PROP_BLUE_DISABLE:5

If you set this to TRUE the effect does not apply the transfer function to the Blue channel. 
          If you set this to FALSE the effect applies the BlueDiscreteTransfer function to the Blue channel.
          

The type is BOOL.

The default value if FALSE.

### -field D2D1_DISCRETETRANSFER_PROP_ALPHA_TABLE:6

The list of values used to define the transfer function for the Alpha channel.
          

The type is FLOAT[].

The default value is {0.0f, 1.0f}.

### -field D2D1_DISCRETETRANSFER_PROP_ALPHA_DISABLE:7

If you set this to TRUE the effect does not apply the transfer function to the Alpha channel. 
          If you set this to FALSE the effect applies the AlphaDiscreteTransfer function to the Alpha channel.
          

The type is BOOL.

The default value if FALSE.

### -field D2D1_DISCRETETRANSFER_PROP_CLAMP_OUTPUT:8

Whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph. 
          The effect clamps the values before it premultiplies the alpha.

          

If you set this to TRUE the effect will clamp the values. If you set this to FALSE, the effect will not clamp the color values, 
          but other effects and the output surface may clamp the values if they are not of high enough precision.

The type is BOOL.

The default value if FALSE.

### -field D2D1_DISCRETETRANSFER_PROP_FORCE_DWORD:0xffffffff
