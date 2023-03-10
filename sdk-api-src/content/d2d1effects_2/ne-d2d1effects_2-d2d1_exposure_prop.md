---
UID: NE:d2d1effects_2.D2D1_EXPOSURE_PROP
title: D2D1_EXPOSURE_PROP (d2d1effects_2.h)
description: Identifiers for properties of the Exposure effect.
helpviewer_keywords: ["D2D1_EXPOSURE_PROP","D2D1_EXPOSURE_PROP enumeration [Direct2D]","D2D1_EXPOSURE_PROP_EXPOSURE_VALUE","d2d1effects_2/D2D1_EXPOSURE_PROP","d2d1effects_2/D2D1_EXPOSURE_PROP_EXPOSURE_VALUE","direct2d.d2d1_exposure_prop"]
old-location: direct2d\d2d1_exposure_prop.htm
tech.root: Direct2D
ms.assetid: 0C294B8B-2E18-48B7-AB81-602AB7949131
ms.date: 01/30/2019
ms.keywords: D2D1_EXPOSURE_PROP, D2D1_EXPOSURE_PROP enumeration [Direct2D], D2D1_EXPOSURE_PROP_EXPOSURE_VALUE, d2d1effects_2/D2D1_EXPOSURE_PROP, d2d1effects_2/D2D1_EXPOSURE_PROP_EXPOSURE_VALUE, direct2d.d2d1_exposure_prop
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
req.typenames: D2D1_EXPOSURE_PROP
req.redist: 
f1_keywords:
 - D2D1_EXPOSURE_PROP
 - d2d1effects_2/D2D1_EXPOSURE_PROP
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
 - D2D1_EXPOSURE_PROP
---

# D2D1_EXPOSURE_PROP enumeration


## -description

Identifiers for properties of the [Exposure effect](/windows/desktop/Direct2D/exposure-effect).

## -enum-fields

### -field D2D1_EXPOSURE_PROP_EXPOSURE_VALUE:0

The D2D1_EXPOSURE_PROP_EXPOSURE_VALUE property is a float value that specifies how much to increase or decrease the exposure of the image. The allowed range is -2.0 to 2.0. The default value is 0.0 (no change).

### -field D2D1_EXPOSURE_PROP_FORCE_DWORD:0xffffffff

