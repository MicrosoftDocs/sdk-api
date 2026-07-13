---
UID: NE:d2d1effects_2.D2D1_WHITELEVELADJUSTMENT_PROP
title: D2D1_WHITELEVELADJUSTMENT_PROP (d2d1effects_2.h)
description: Defines constants that identify the top level properties of the White Level Adjustment effect.
helpviewer_keywords: ["D2D1_WHITELEVELADJUSTMENT_PROP","D2D1_WHITELEVELADJUSTMENT_PROP enumeration [Direct2D]","D2D1_WHITELEVELADJUSTMENT_PROP_INPUT_WHITE_LEVEL","D2D1_WHITELEVELADJUSTMENT_PROP_OUTPUT_WHITE_LEVEL","d2d1effects_2/D2D1_WHITELEVELADJUSTMENT_PROP","d2d1effects_2/D2D1_WHITELEVELADJUSTMENT_PROP_INPUT_WHITE_LEVEL","d2d1effects_2/D2D1_WHITELEVELADJUSTMENT_PROP_OUTPUT_WHITE_LEVEL","direct2d.d2d1_whiteleveladjustment_prop"]
old-location: direct2d\d2d1_whiteleveladjustment_prop.htm
tech.root: Direct2D
ms.date: 01/30/2019
ms.keywords: D2D1_WHITELEVELADJUSTMENT_PROP, D2D1_WHITELEVELADJUSTMENT_PROP enumeration [Direct2D], D2D1_WHITELEVELADJUSTMENT_PROP_INPUT_WHITE_LEVEL, D2D1_WHITELEVELADJUSTMENT_PROP_OUTPUT_WHITE_LEVEL, d2d1effects_2/D2D1_WHITELEVELADJUSTMENT_PROP, d2d1effects_2/D2D1_WHITELEVELADJUSTMENT_PROP_INPUT_WHITE_LEVEL, d2d1effects_2/D2D1_WHITELEVELADJUSTMENT_PROP_OUTPUT_WHITE_LEVEL, direct2d.d2d1_whiteleveladjustment_prop
req.header: d2d1effects_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
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
req.typenames: D2D1_WHITELEVELADJUSTMENT_PROP
req.redist: 
f1_keywords:
 - D2D1_WHITELEVELADJUSTMENT_PROP
 - d2d1effects_2/D2D1_WHITELEVELADJUSTMENT_PROP
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
 - D2D1_WHITELEVELADJUSTMENT_PROP
---

# D2D1_WHITELEVELADJUSTMENT_PROP enumeration


## -description

Defines constants that identify the top level properties of the [White level adjustment effect](/windows/desktop/Direct2D/white-level-adjustment-effect). The effect adjusts the white level of the source image by multiplying the source image color by the ratio of the input and output white levels. Input and output white levels are specified in nits.

## -enum-fields

### -field D2D1_WHITELEVELADJUSTMENT_PROP_INPUT_WHITE_LEVEL (0)

Identifies the `InputWhiteLevel` property of the effect. The property is of type FLOAT, and is specified in nits.

### -field D2D1_WHITELEVELADJUSTMENT_PROP_OUTPUT_WHITE_LEVEL (1)

Identifies the `OutputWhiteLevel` property of the effect. The property is of type FLOAT, and is specified in nits.

### -field D2D1_WHITELEVELADJUSTMENT_PROP_FORCE_DWORD (0xFFFFFFFF)

