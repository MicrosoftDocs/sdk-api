---
UID: NE:d2d1effects_2.D2D1_TEMPERATUREANDTINT_PROP
title: D2D1_TEMPERATUREANDTINT_PROP (d2d1effects_2.h)
description: Identifiers for properties of the Temperature and Tint effect.
helpviewer_keywords: ["D2D1_TEMPERATUREANDTINT_PROP","D2D1_TEMPERATUREANDTINT_PROP enumeration [Direct2D]","D2D1_TEMPERATUREANDTINT_PROP_TEMPERATURE","D2D1_TEMPERATUREANDTINT_PROP_TINT","d2d1effects_2/D2D1_TEMPERATUREANDTINT_PROP","d2d1effects_2/D2D1_TEMPERATUREANDTINT_PROP_TEMPERATURE","d2d1effects_2/D2D1_TEMPERATUREANDTINT_PROP_TINT","direct2d.d2d1_temperatureandtint_prop"]
old-location: direct2d\d2d1_temperatureandtint_prop.htm
tech.root: Direct2D
ms.assetid: 7295BFD0-773A-488A-BE86-CE1B202BCAC6
ms.date: 12/05/2018
ms.keywords: D2D1_TEMPERATUREANDTINT_PROP, D2D1_TEMPERATUREANDTINT_PROP enumeration [Direct2D], D2D1_TEMPERATUREANDTINT_PROP_TEMPERATURE, D2D1_TEMPERATUREANDTINT_PROP_TINT, d2d1effects_2/D2D1_TEMPERATUREANDTINT_PROP, d2d1effects_2/D2D1_TEMPERATUREANDTINT_PROP_TEMPERATURE, d2d1effects_2/D2D1_TEMPERATUREANDTINT_PROP_TINT, direct2d.d2d1_temperatureandtint_prop
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
req.typenames: D2D1_TEMPERATUREANDTINT_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_TEMPERATUREANDTINT_PROP
 - d2d1effects_2/D2D1_TEMPERATUREANDTINT_PROP
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
 - D2D1_TEMPERATUREANDTINT_PROP
---

# D2D1_TEMPERATUREANDTINT_PROP enumeration


## -description

Identifiers for properties of the <a href="/windows/desktop/Direct2D/temperature-and-tint-effect">Temperature and Tint effect</a>.

## -enum-fields

### -field D2D1_TEMPERATUREANDTINT_PROP_TEMPERATURE:0

The D2D1_TEMPERATUREANDTINT_PROP_TEMPERATURE property is a float value specifying how much to increase or decrease the temperature of the input image.  The allowed range is -1.0 to 1.0. The default value is 0.0.

### -field D2D1_TEMPERATUREANDTINT_PROP_TINT:1

The D2D1_TEMPERATUREANDTINT_PROP_TINT property is a float value specifying how much to increase or decrease the tint of the input image.  The allowed range is -1.0 to 1.0.  The default value is 0.0.

### -field D2D1_TEMPERATUREANDTINT_PROP_FORCE_DWORD:0xffffffff
