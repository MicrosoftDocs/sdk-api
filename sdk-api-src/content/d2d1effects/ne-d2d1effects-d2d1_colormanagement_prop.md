---
UID: NE:d2d1effects.D2D1_COLORMANAGEMENT_PROP
title: D2D1_COLORMANAGEMENT_PROP
author: windows-sdk-content
description: Identifiers for the properties of the Color management effect.
old-location: direct2d\d2d1_colormanagement_prop.htm
tech.root: direct2d
ms.assetid: 1003B981-5F12-4CE9-B4A5-2E96CAEE6AC8
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: D2D1_COLORMANAGEMENT_PROP, D2D1_COLORMANAGEMENT_PROP enumeration [Direct2D], D2D1_COLORMANAGEMENT_PROP_ALPHA_MODE, D2D1_COLORMANAGEMENT_PROP_DESTINATION_COLOR_CONTEXT, D2D1_COLORMANAGEMENT_PROP_DESTINATION_RENDERING_INTENT, D2D1_COLORMANAGEMENT_PROP_QUALITY, D2D1_COLORMANAGEMENT_PROP_SOURCE_COLOR_CONTEXT, D2D1_COLORMANAGEMENT_PROP_SOURCE_RENDERING_INTENT, d2d1effects/D2D1_COLORMANAGEMENT_PROP, d2d1effects/D2D1_COLORMANAGEMENT_PROP_ALPHA_MODE, d2d1effects/D2D1_COLORMANAGEMENT_PROP_DESTINATION_COLOR_CONTEXT, d2d1effects/D2D1_COLORMANAGEMENT_PROP_DESTINATION_RENDERING_INTENT, d2d1effects/D2D1_COLORMANAGEMENT_PROP_QUALITY, d2d1effects/D2D1_COLORMANAGEMENT_PROP_SOURCE_COLOR_CONTEXT, d2d1effects/D2D1_COLORMANAGEMENT_PROP_SOURCE_RENDERING_INTENT, direct2d.d2d1_colormanagement_prop
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
 - D2D1_COLORMANAGEMENT_PROP
product: Windows
targetos: Windows
req.typenames: D2D1_COLORMANAGEMENT_PROP
req.redist: 
---

# D2D1_COLORMANAGEMENT_PROP enumeration


## -description


Identifiers for the properties of the <a href="https://msdn.microsoft.com/en-us/library/Hh706318(v=VS.85).aspx">Color management effect</a>.
        


## -enum-fields




### -field D2D1_COLORMANAGEMENT_PROP_SOURCE_COLOR_CONTEXT

The source color space information. 
          

The type is <a href="https://msdn.microsoft.com/acdda11e-eb3f-4258-b24e-daa3b7a23fd6">ID2D1ColorContext</a>.

The default value is NULL.


### -field D2D1_COLORMANAGEMENT_PROP_SOURCE_RENDERING_INTENT

Which ICC rendering intent to use. 
          

The type is <a href="https://msdn.microsoft.com/en-us/library/Dn934228(v=VS.85).aspx">D2D1_COLORMANAGEMENT_RENDERING_INTENT</a>.

The default value is D2D1_COLORMANAGEMENT_RENDERING_INTENT_PERCEPTUAL.


### -field D2D1_COLORMANAGEMENT_PROP_DESTINATION_COLOR_CONTEXT

The destination color space information. 
          

The type is <a href="https://msdn.microsoft.com/acdda11e-eb3f-4258-b24e-daa3b7a23fd6">ID2D1ColorContext</a>.

The default value is NULL.


### -field D2D1_COLORMANAGEMENT_PROP_DESTINATION_RENDERING_INTENT

Which ICC rendering intent to use. 
          

The type is <a href="https://msdn.microsoft.com/en-us/library/Dn934228(v=VS.85).aspx">D2D1_COLORMANAGEMENT_RENDERING_INTENT</a>.

The default value is D2D1_COLORMANAGEMENT_RENDERING_INTENT_PERCEPTUAL.


### -field D2D1_COLORMANAGEMENT_PROP_ALPHA_MODE

How to interpret alpha data that is contained in the input image. 
          

The type is <a href="https://msdn.microsoft.com/en-us/library/Dn934225(v=VS.85).aspx">D2D1_COLORMANAGEMENT_ALPHA_MODE</a>.

The default value is D2D1_COLORMANAGEMENT_ALPHA_MODE_PREMULTIPLIED.


### -field D2D1_COLORMANAGEMENT_PROP_QUALITY

The quality level of the transform. 
          

The type is <a href="https://msdn.microsoft.com/en-us/library/Dn934227(v=VS.85).aspx">D2D1_COLORMANAGEMENT_QUALITY</a>.

The default value is D2D1_COLORMANAGEMENT_QUALITY_NORMAL.


### -field D2D1_COLORMANAGEMENT_PROP_FORCE_DWORD



