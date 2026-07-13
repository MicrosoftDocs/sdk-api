---
UID: NE:d2d1effects_2.D2D1_SHARPEN_PROP
title: D2D1_SHARPEN_PROP (d2d1effects_2.h)
description: Identifiers for properties of the Sharpen effect.
helpviewer_keywords: ["D2D1_SHARPEN_PROP","D2D1_SHARPEN_PROP enumeration [Direct2D]","D2D1_SHARPEN_PROP_SHARPNESS","D2D1_SHARPEN_PROP_THRESHOLD","d2d1effects_2/D2D1_SHARPEN_PROP","d2d1effects_2/D2D1_SHARPEN_PROP_SHARPNESS","d2d1effects_2/D2D1_SHARPEN_PROP_THRESHOLD","direct2d.d2d1_sharpen_prop"]
old-location: direct2d\d2d1_sharpen_prop.htm
tech.root: Direct2D
ms.assetid: 73ED06C4-A8FB-4312-8BB8-3B9C885E9FEC
ms.date: 12/05/2018
ms.keywords: D2D1_SHARPEN_PROP, D2D1_SHARPEN_PROP enumeration [Direct2D], D2D1_SHARPEN_PROP_SHARPNESS, D2D1_SHARPEN_PROP_THRESHOLD, d2d1effects_2/D2D1_SHARPEN_PROP, d2d1effects_2/D2D1_SHARPEN_PROP_SHARPNESS, d2d1effects_2/D2D1_SHARPEN_PROP_THRESHOLD, direct2d.d2d1_sharpen_prop
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
req.typenames: D2D1_SHARPEN_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_SHARPEN_PROP
 - d2d1effects_2/D2D1_SHARPEN_PROP
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
 - D2D1_SHARPEN_PROP
---

# D2D1_SHARPEN_PROP enumeration


## -description

Identifiers for properties of the <a href="/windows/desktop/Direct2D/sharpen-effect">Sharpen effect</a>.

## -enum-fields

### -field D2D1_SHARPEN_PROP_SHARPNESS:0

The D2D1_SHARPEN_PROP_SHARPNESS property is a float value indicating how much to sharpen the input image.  The allowed range is 0.0 to 10.0. The default value is 0.0.

### -field D2D1_SHARPEN_PROP_THRESHOLD:1

The D2D1_SHARPEN_PROP_THRESHOLD property is a float value.  The allowed range is 0.0 to 1.0. The default value is 0.0.

### -field D2D1_SHARPEN_PROP_FORCE_DWORD:0xffffffff
