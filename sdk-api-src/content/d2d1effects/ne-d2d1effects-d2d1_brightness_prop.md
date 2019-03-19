---
UID: NE:d2d1effects.D2D1_BRIGHTNESS_PROP
title: D2D1_BRIGHTNESS_PROP (d2d1effects.h)
author: windows-sdk-content
description: Identifiers for the properties of the Brightness effect.
old-location: direct2d\d2d1_brightness_prop.htm
tech.root: Direct2D
ms.assetid: 7D3CEF7A-AF72-451B-8E6A-A9DF8E85EDE9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D2D1_BRIGHTNESS_PROP, D2D1_BRIGHTNESS_PROP enumeration [Direct2D], D2D1_BRIGHTNESS_PROP_BLACK_POINT, D2D1_BRIGHTNESS_PROP_WHITE_POINT, d2d1effects/D2D1_BRIGHTNESS_PROP, d2d1effects/D2D1_BRIGHTNESS_PROP_BLACK_POINT, d2d1effects/D2D1_BRIGHTNESS_PROP_WHITE_POINT, direct2d.d2d1_brightness_prop
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
 - D2D1_BRIGHTNESS_PROP
product: Windows
targetos: Windows
req.typenames: D2D1_BRIGHTNESS_PROP
req.redist: 
---

# D2D1_BRIGHTNESS_PROP enumeration


## -description


Identifiers for the properties of the <a href="https://msdn.microsoft.com/5088D4D4-DFC8-45D3-B1C3-D576742D931C">Brightness effect</a>.


## -enum-fields




### -field D2D1_BRIGHTNESS_PROP_WHITE_POINT

The upper portion of the brightness transfer curve. The white point adjusts the appearance of the brighter portions of the image. 
          This property is for both the x value and the y value, in that order. Each of the values of this property are between 0 and 1, inclusive.
          

The type is <a href="https://msdn.microsoft.com/DD180090-D2F4-4DF3-8652-101713C01AE4">D2D1_VECTOR_2F</a>.

The default value is (1.0f, 1.0f).


### -field D2D1_BRIGHTNESS_PROP_BLACK_POINT

The lower portion of the brightness transfer curve. The black point adjusts the appearance of the darker portions of the image. 
          This property is for both the x value and the y value, in that order. Each of the values of this property are between 0 and 1, inclusive.
          

The type is <a href="https://msdn.microsoft.com/DD180090-D2F4-4DF3-8652-101713C01AE4">D2D1_VECTOR_2F</a>.

The default value is (0.0f, 0.0f).


### -field D2D1_BRIGHTNESS_PROP_FORCE_DWORD



