---
UID: NE:d2d1effects.D2D1_GAMMATRANSFER_PROP
title: D2D1_GAMMATRANSFER_PROP (d2d1effects.h)
author: windows-sdk-content
description: Identifiers for properties of the Gamma transfer effect.
old-location: direct2d\d2d1_gammatransfer_prop.htm
tech.root: Direct2D
ms.assetid: 3A2344BC-8A47-45E7-B26A-8124892F3F27
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D2D1_GAMMATRANSFER_PROP, D2D1_GAMMATRANSFER_PROP enumeration [Direct2D], D2D1_GAMMATRANSFER_PROP_ALPHA_AMPLITUDE, D2D1_GAMMATRANSFER_PROP_ALPHA_DISABLE, D2D1_GAMMATRANSFER_PROP_ALPHA_EXPONENT, D2D1_GAMMATRANSFER_PROP_ALPHA_OFFSET, D2D1_GAMMATRANSFER_PROP_BLUE_AMPLITUDE, D2D1_GAMMATRANSFER_PROP_BLUE_DISABLE, D2D1_GAMMATRANSFER_PROP_BLUE_EXPONENT, D2D1_GAMMATRANSFER_PROP_BLUE_OFFSET, D2D1_GAMMATRANSFER_PROP_CLAMP_OUTPUT, D2D1_GAMMATRANSFER_PROP_GREEN_AMPLITUDE, D2D1_GAMMATRANSFER_PROP_GREEN_DISABLE, D2D1_GAMMATRANSFER_PROP_GREEN_EXPONENT, D2D1_GAMMATRANSFER_PROP_GREEN_OFFSET, D2D1_GAMMATRANSFER_PROP_RED_AMPLITUDE, D2D1_GAMMATRANSFER_PROP_RED_DISABLE, D2D1_GAMMATRANSFER_PROP_RED_EXPONENT, D2D1_GAMMATRANSFER_PROP_RED_OFFSET, d2d1effects/D2D1_GAMMATRANSFER_PROP, d2d1effects/D2D1_GAMMATRANSFER_PROP_ALPHA_AMPLITUDE, d2d1effects/D2D1_GAMMATRANSFER_PROP_ALPHA_DISABLE, d2d1effects/D2D1_GAMMATRANSFER_PROP_ALPHA_EXPONENT, d2d1effects/D2D1_GAMMATRANSFER_PROP_ALPHA_OFFSET, d2d1effects/D2D1_GAMMATRANSFER_PROP_BLUE_AMPLITUDE, d2d1effects/D2D1_GAMMATRANSFER_PROP_BLUE_DISABLE, d2d1effects/D2D1_GAMMATRANSFER_PROP_BLUE_EXPONENT, d2d1effects/D2D1_GAMMATRANSFER_PROP_BLUE_OFFSET, d2d1effects/D2D1_GAMMATRANSFER_PROP_CLAMP_OUTPUT, d2d1effects/D2D1_GAMMATRANSFER_PROP_GREEN_AMPLITUDE, d2d1effects/D2D1_GAMMATRANSFER_PROP_GREEN_DISABLE, d2d1effects/D2D1_GAMMATRANSFER_PROP_GREEN_EXPONENT, d2d1effects/D2D1_GAMMATRANSFER_PROP_GREEN_OFFSET, d2d1effects/D2D1_GAMMATRANSFER_PROP_RED_AMPLITUDE, d2d1effects/D2D1_GAMMATRANSFER_PROP_RED_DISABLE, d2d1effects/D2D1_GAMMATRANSFER_PROP_RED_EXPONENT, d2d1effects/D2D1_GAMMATRANSFER_PROP_RED_OFFSET, direct2d.d2d1_gammatransfer_prop
ms.topic: enum
f1_keywords: 
 - "d2d1effects/D2D1_GAMMATRANSFER_PROP"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1effects.h
api_name:
 - D2D1_GAMMATRANSFER_PROP
targetos: Windows
req.typenames: D2D1_GAMMATRANSFER_PROP
req.redist: 
ms.custom: 19H1
---

# D2D1_GAMMATRANSFER_PROP enumeration


## -description


Identifiers for properties of the <a href="https://docs.microsoft.com/windows/desktop/Direct2D/gamma-transfer">Gamma transfer effect</a>.
        


## -enum-fields




### -field D2D1_GAMMATRANSFER_PROP_RED_AMPLITUDE

The amplitude of the gamma transfer function for the Red channel.
            

The type is FLOAT.

The default value is 1.0f.


### -field D2D1_GAMMATRANSFER_PROP_RED_EXPONENT

The exponent of the gamma transfer function for the Red channel.
            

The type is FLOAT.

The default value is 1.0f.


### -field D2D1_GAMMATRANSFER_PROP_RED_OFFSET

The offset of the gamma transfer function for the Red channel.
            

The type is FLOAT.

The default value is 0.0f.


### -field D2D1_GAMMATRANSFER_PROP_RED_DISABLE

If you set this to TRUE it does not apply the transfer function to the Red channel. An identity transfer function is used.
            If you set this to FALSE it applies the gamma transfer function to the Red channel.
            

The type is BOOL.

The default value is FALSE.


### -field D2D1_GAMMATRANSFER_PROP_GREEN_AMPLITUDE

The amplitude of the gamma transfer function for the Green channel.
            

The type is FLOAT.

The default value is 1.0f.


### -field D2D1_GAMMATRANSFER_PROP_GREEN_EXPONENT

The exponent of the gamma transfer function for the Green channel.
            

The type is FLOAT.

The default value is 1.0f.


### -field D2D1_GAMMATRANSFER_PROP_GREEN_OFFSET

The offset of the gamma transfer function for the Green channel.
            

The type is FLOAT.

The default value is 0.0f.


### -field D2D1_GAMMATRANSFER_PROP_GREEN_DISABLE

If you set this to TRUE it does not apply the transfer function to the Green channel. An identity transfer function is used.
            If you set this to FALSE it applies the gamma transfer function to the Green channel.
            

The type is BOOL.

The default value is FALSE.


### -field D2D1_GAMMATRANSFER_PROP_BLUE_AMPLITUDE

The amplitude of the gamma transfer function for the Blue channel.
            

The type is FLOAT.

The default value is 1.0f.


### -field D2D1_GAMMATRANSFER_PROP_BLUE_EXPONENT

The exponent of the gamma transfer function for the Blue channel.
            

The type is FLOAT.

The default value is 1.0f.


### -field D2D1_GAMMATRANSFER_PROP_BLUE_OFFSET

The offset of the gamma transfer function for the Blue channel.
            

The type is FLOAT.

The default value is 0.0f.


### -field D2D1_GAMMATRANSFER_PROP_BLUE_DISABLE

If you set this to TRUE it does not apply the transfer function to the Blue channel. An identity transfer function is used.
            If you set this to FALSE it applies the gamma transfer function to the Blue channel.
            

The type is BOOL.

The default value is FALSE.


### -field D2D1_GAMMATRANSFER_PROP_ALPHA_AMPLITUDE

The amplitude of the gamma transfer function for the Alpha channel.
            

The type is FLOAT.

The default value is 1.0f.


### -field D2D1_GAMMATRANSFER_PROP_ALPHA_EXPONENT

The exponent of the gamma transfer function for the Alpha channel.
            

The type is FLOAT.

The default value is 1.0f.


### -field D2D1_GAMMATRANSFER_PROP_ALPHA_OFFSET

The offset of the gamma transfer function for the Alpha channel.
            

The type is FLOAT.

The default value is 0.0f.


### -field D2D1_GAMMATRANSFER_PROP_ALPHA_DISABLE

If you set this to TRUE it does not apply the transfer function to the Alpha channel. An identity transfer function is used.
            If you set this to FALSE it applies the gamma transfer function to the Alpha channel.
            

The type is BOOL.

The default value is FALSE.


### -field D2D1_GAMMATRANSFER_PROP_CLAMP_OUTPUT

Whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.
            The effect clamps the values before it premultiplies the alpha.
            

If you set this to TRUE the effect will clamp the values. If you set this to FALSE, the effect will not clamp the color values,
              but other effects and the output surface may clamp the values if they are not of high enough precision.
            

The type is BOOL.

The default value is FALSE.


### -field D2D1_GAMMATRANSFER_PROP_FORCE_DWORD



