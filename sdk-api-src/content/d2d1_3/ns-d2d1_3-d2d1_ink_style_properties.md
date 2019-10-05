---
UID: NS:d2d1_3.D2D1_INK_STYLE_PROPERTIES
title: D2D1_INK_STYLE_PROPERTIES (d2d1_3.h)
author: windows-sdk-content
description: Defines the general pen tip shape and the transform used in an ID2D1InkStyle object.
old-location: direct2d\d2d1_ink_style_properties.htm
tech.root: Direct2D
ms.assetid: 81B9E108-D0A6-4F7E-8BE9-76A570B1D050
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D2D1_INK_STYLE_PROPERTIES, D2D1_INK_STYLE_PROPERTIES structure [Direct2D], d2d1_3/D2D1_INK_STYLE_PROPERTIES, direct2d.d2d1_ink_style_properties
ms.topic: struct
f1_keywords: 
 - "d2d1_3/D2D1_INK_STYLE_PROPERTIES"
dev_langs:
 - c++
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
 - D2D1_INK_STYLE_PROPERTIES
targetos: Windows
req.typenames: D2D1_INK_STYLE_PROPERTIES
req.redist: 
ms.custom: 19H1
---

# D2D1_INK_STYLE_PROPERTIES structure


## -description


Defines the general pen tip shape and the transform used in an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1inkstyle">ID2D1InkStyle</a> object.
        


## -struct-fields




### -field nibShape

The pre-transform shape of the nib (pen tip) used to draw a given ink object.


### -field nibTransform

The transform applied to the nib.  Note that the translation components of the transform matrix are ignored for the purposes of rendering.
          

