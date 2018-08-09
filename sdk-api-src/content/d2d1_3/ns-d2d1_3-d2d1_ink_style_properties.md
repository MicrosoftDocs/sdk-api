---
UID: NS:d2d1_3.D2D1_INK_STYLE_PROPERTIES
title: D2D1_INK_STYLE_PROPERTIES
author: windows-sdk-content
description: Defines the general pen tip shape and the transform used in an ID2D1InkStyle object.
old-location: direct2d\d2d1_ink_style_properties.htm
old-project: direct2d
ms.assetid: 81B9E108-D0A6-4F7E-8BE9-76A570B1D050
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: D2D1_INK_STYLE_PROPERTIES, D2D1_INK_STYLE_PROPERTIES structure [Direct2D], d2d1_3/D2D1_INK_STYLE_PROPERTIES, direct2d.d2d1_ink_style_properties
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D2D1_INK_STYLE_PROPERTIES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1_3.h
api_name:
 - D2D1_INK_STYLE_PROPERTIES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D2D1_INK_STYLE_PROPERTIES structure


## -description


Defines the general pen tip shape and the transform used in an <a href="https://msdn.microsoft.com/03853FA5-1377-42FB-A4C2-50069DDF6E2D">ID2D1InkStyle</a> object.
        


## -struct-fields




### -field nibShape

The pre-transform shape of the nib (pen tip) used to draw a given ink object.


### -field nibTransform

The transform applied to the nib.  Note that the translation components of the transform matrix are ignored for the purposes of rendering.
          

