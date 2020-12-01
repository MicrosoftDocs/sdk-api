---
UID: NS:d2d1_1.D2D1_PRINT_CONTROL_PROPERTIES
title: D2D1_PRINT_CONTROL_PROPERTIES (d2d1_1.h)
description: The creation properties for a ID2D1PrintControl object.
helpviewer_keywords: ["D2D1_PRINT_CONTROL_PROPERTIES","D2D1_PRINT_CONTROL_PROPERTIES structure [Direct2D]","d2d1_1/D2D1_PRINT_CONTROL_PROPERTIES","direct2d.d2d1_print_control_properties"]
old-location: direct2d\d2d1_print_control_properties.htm
tech.root: Direct2D
ms.assetid: 5A4D4DDC-4161-44A2-9EB6-E4C14696B810
ms.date: 12/05/2018
ms.keywords: D2D1_PRINT_CONTROL_PROPERTIES, D2D1_PRINT_CONTROL_PROPERTIES structure [Direct2D], d2d1_1/D2D1_PRINT_CONTROL_PROPERTIES, direct2d.d2d1_print_control_properties
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: D2D1.lib
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D2D1_PRINT_CONTROL_PROPERTIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_PRINT_CONTROL_PROPERTIES
 - d2d1_1/D2D1_PRINT_CONTROL_PROPERTIES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - D2D1.lib
api_name:
 - D2D1_PRINT_CONTROL_PROPERTIES
---

# D2D1_PRINT_CONTROL_PROPERTIES structure


## -description

The creation properties for a <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1printcontrol">ID2D1PrintControl</a> object.

## -struct-fields

### -field fontSubset

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_print_font_subset_mode">D2D1_PRINT_FONT_SUBSET_MODE</a></b>

The mode to use for subsetting fonts for printing, defaults to <a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_print_font_subset_mode">D2D1_PRINT_FONT_SUBSET_MODE_DEFAULT</a>.

### -field rasterDPI

Type: <b>FLOAT</b>

DPI for rasterization of all unsupported Direct2D commands or options, defaults to 150.0.

### -field colorSpace

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_color_space">D2D1_COLOR_SPACE</a></b>

Color space for vector graphics, defaults to <a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_color_space">D2D1_COLOR_SPACE_SRGB</a>.