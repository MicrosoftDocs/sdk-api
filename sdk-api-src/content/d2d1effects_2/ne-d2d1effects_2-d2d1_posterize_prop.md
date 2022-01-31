---
UID: NE:d2d1effects_2.D2D1_POSTERIZE_PROP
title: D2D1_POSTERIZE_PROP (d2d1effects_2.h)
description: Identifiers for properties of the Posterize effect.
helpviewer_keywords: ["D2D1_POSTERIZE_PROP","D2D1_POSTERIZE_PROP enumeration [Direct2D]","D2D1_POSTERIZE_PROP_BLUE_VALUE_COUNT","D2D1_POSTERIZE_PROP_GREEN_VALUE_COUNT","D2D1_POSTERIZE_PROP_RED_VALUE_COUNT","d2d1effects_2/D2D1_POSTERIZE_PROP","d2d1effects_2/D2D1_POSTERIZE_PROP_BLUE_VALUE_COUNT","d2d1effects_2/D2D1_POSTERIZE_PROP_GREEN_VALUE_COUNT","d2d1effects_2/D2D1_POSTERIZE_PROP_RED_VALUE_COUNT","direct2d.d2d1_posterize_prop"]
old-location: direct2d\d2d1_posterize_prop.htm
tech.root: Direct2D
ms.assetid: F5A41C61-6AEB-47A6-813E-FF19994D013D
ms.date: 12/05/2018
ms.keywords: D2D1_POSTERIZE_PROP, D2D1_POSTERIZE_PROP enumeration [Direct2D], D2D1_POSTERIZE_PROP_BLUE_VALUE_COUNT, D2D1_POSTERIZE_PROP_GREEN_VALUE_COUNT, D2D1_POSTERIZE_PROP_RED_VALUE_COUNT, d2d1effects_2/D2D1_POSTERIZE_PROP, d2d1effects_2/D2D1_POSTERIZE_PROP_BLUE_VALUE_COUNT, d2d1effects_2/D2D1_POSTERIZE_PROP_GREEN_VALUE_COUNT, d2d1effects_2/D2D1_POSTERIZE_PROP_RED_VALUE_COUNT, direct2d.d2d1_posterize_prop
req.header: d2d1effects_2.h
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
req.typenames: D2D1_POSTERIZE_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_POSTERIZE_PROP
 - d2d1effects_2/D2D1_POSTERIZE_PROP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1effects_2.h
api_name:
 - D2D1_POSTERIZE_PROP
---

# D2D1_POSTERIZE_PROP enumeration


## -description

Identifiers for properties of the <a href="/windows/desktop/Direct2D/posterize-effect">Posterize effect</a>.

## -enum-fields

### -field D2D1_POSTERIZE_PROP_RED_VALUE_COUNT:0

The D2D1_POSTERIZE_PROP_RED_VALUE_COUNT property is an integer value specifying how many evenly spaced steps to divide the red channel range of 0.0 to 1.0 into.  
          For example, a value of 4 generates a table with 4 steps, [0.0, 0.33, 0.67, 1.0].  The allowed range for this property is 2 to 16.  The default value is 4.

### -field D2D1_POSTERIZE_PROP_GREEN_VALUE_COUNT:1

The D2D1_POSTERIZE_PROP_GREEN_VALUE_COUNT property is an integer value specifying how many evenly spaced steps to divide the green channel range of 0.0 to 1.0 into.  
          For example, a value of 4 generates a table with 4 steps, [0.0, 0.33, 0.67, 1.0].  The allowed range for this property is 2 to 16.  The default value is 4.

### -field D2D1_POSTERIZE_PROP_BLUE_VALUE_COUNT:2

The D2D1_POSTERIZE_PROP_BLUE_VALUE_COUNT property is an integer value specifying how many evenly spaced steps to divide the blue channel range of 0.0 to 1.0 into.  
          For example, a value of 4 generates a table with 4 steps, [0.0, 0.33, 0.67, 1.0].  The allowed range for this property is 2 to 16.  The default value is 4.

### -field D2D1_POSTERIZE_PROP_FORCE_DWORD:0xffffffff
