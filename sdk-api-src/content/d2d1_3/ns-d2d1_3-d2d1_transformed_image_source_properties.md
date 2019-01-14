---
UID: NS:d2d1_3.D2D1_TRANSFORMED_IMAGE_SOURCE_PROPERTIES
title: D2D1_TRANSFORMED_IMAGE_SOURCE_PROPERTIES
author: windows-sdk-content
description: Properties of a transformed image source.
old-location: direct2d\d2d1_transformed_image_source_properties.htm
tech.root: Direct2D
ms.assetid: E8A39769-07F2-42CA-A7CA-F83FF97E2076
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D2D1_TRANSFORMED_IMAGE_SOURCE_PROPERTIES, D2D1_TRANSFORMED_IMAGE_SOURCE_PROPERTIES structure [Direct2D], d2d1_3/D2D1_TRANSFORMED_IMAGE_SOURCE_PROPERTIES, direct2d.d2d1_transformed_image_source_properties
ms.topic: struct
req.header: d2d1_3.h
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
 - d2d1_3.h
api_name:
 - D2D1_TRANSFORMED_IMAGE_SOURCE_PROPERTIES
product: Windows
targetos: Windows
req.typenames: D2D1_TRANSFORMED_IMAGE_SOURCE_PROPERTIES
req.redist: 
---

# D2D1_TRANSFORMED_IMAGE_SOURCE_PROPERTIES structure


## -description


Properties of a transformed image source.


## -struct-fields




### -field orientation

Type: <b><a href="https://msdn.microsoft.com/CFDE26F2-2D10-4B7E-A7B0-A2A86923116E">D2D1_ORIENTATION</a></b>

The orientation at which the image source is drawn.


### -field scaleX

Type: <b>FLOAT</b>

The horizontal scale factor at which the image source is drawn.


### -field scaleY

Type: <b>FLOAT</b>

The vertical scale factor at which the image source is drawn.


### -field interpolationMode

Type: <b><a href="https://msdn.microsoft.com/7a32f551-afad-4eb2-953f-a9acc71d7776">D2D1_INTERPOLATION_MODE</a></b>

The interpolation mode used when the image source is drawn.  This is ignored if the image source is drawn using the DrawImage method, or using an image brush.


### -field options

Type: <b><a href="https://msdn.microsoft.com/25A55F80-ACE0-4955-8483-687C7A7E4E20">D2D1_TRANSFORMED_IMAGE_SOURCE_OPTIONS</a></b>

Image sourc option flags.

