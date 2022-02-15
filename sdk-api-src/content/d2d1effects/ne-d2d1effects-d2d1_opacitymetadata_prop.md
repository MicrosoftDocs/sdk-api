---
UID: NE:d2d1effects.D2D1_OPACITYMETADATA_PROP
title: D2D1_OPACITYMETADATA_PROP (d2d1effects.h)
description: Identifiers for properties of the Opacity metadata effect.
helpviewer_keywords: ["D2D1_OPACITYMETADATA_PROP","D2D1_OPACITYMETADATA_PROP enumeration [Direct2D]","D2D1_OPACITYMETADATA_PROP_INPUT_OPAQUE_RECT","d2d1effects/D2D1_OPACITYMETADATA_PROP","d2d1effects/D2D1_OPACITYMETADATA_PROP_INPUT_OPAQUE_RECT","direct2d.d2d1_opacitymetadata_prop"]
old-location: direct2d\d2d1_opacitymetadata_prop.htm
tech.root: Direct2D
ms.assetid: D8BA5767-EDB0-4BD0-9B07-9009DB1FD678
ms.date: 12/05/2018
ms.keywords: D2D1_OPACITYMETADATA_PROP, D2D1_OPACITYMETADATA_PROP enumeration [Direct2D], D2D1_OPACITYMETADATA_PROP_INPUT_OPAQUE_RECT, d2d1effects/D2D1_OPACITYMETADATA_PROP, d2d1effects/D2D1_OPACITYMETADATA_PROP_INPUT_OPAQUE_RECT, direct2d.d2d1_opacitymetadata_prop
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
targetos: Windows
req.typenames: D2D1_OPACITYMETADATA_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_OPACITYMETADATA_PROP
 - d2d1effects/D2D1_OPACITYMETADATA_PROP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1effects.h
api_name:
 - D2D1_OPACITYMETADATA_PROP
---

# D2D1_OPACITYMETADATA_PROP enumeration


## -description

Identifiers for properties of the <a href="/windows/desktop/Direct2D/opacity-metadata-effect">Opacity metadata effect</a>.

## -enum-fields

### -field D2D1_OPACITYMETADATA_PROP_INPUT_OPAQUE_RECT:0

The portion of the source image that is opaque. The default is the entire input image.
          

The type is <a href="/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_4f">D2D1_VECTOR_4F</a>.

The default is {-FLT_MAX, -FLT_MAX, FLT_MAX, FLT_MAX}.

### -field D2D1_OPACITYMETADATA_PROP_FORCE_DWORD:0xffffffff
