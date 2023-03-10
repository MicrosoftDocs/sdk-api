---
UID: NE:d2d1_3.D2D1_TRANSFORMED_IMAGE_SOURCE_OPTIONS
title: D2D1_TRANSFORMED_IMAGE_SOURCE_OPTIONS (d2d1_3.h)
description: Option flags for transformed image sources.
helpviewer_keywords: ["D2D1_TRANSFORMED_IMAGE_SOURCE_OPTIONS","D2D1_TRANSFORMED_IMAGE_SOURCE_OPTIONS enumeration [Direct2D]","D2D1_TRANSFORMED_IMAGE_SOURCE_OPTIONS_DISABLE_DPI_SCALE","D2D1_TRANSFORMED_IMAGE_SOURCE_OPTIONS_NONE","d2d1_3/D2D1_TRANSFORMED_IMAGE_SOURCE_OPTIONS","d2d1_3/D2D1_TRANSFORMED_IMAGE_SOURCE_OPTIONS_DISABLE_DPI_SCALE","d2d1_3/D2D1_TRANSFORMED_IMAGE_SOURCE_OPTIONS_NONE","direct2d.d2d1_transformed_image_source_options"]
old-location: direct2d\d2d1_transformed_image_source_options.htm
tech.root: Direct2D
ms.assetid: 25A55F80-ACE0-4955-8483-687C7A7E4E20
ms.date: 12/05/2018
ms.keywords: D2D1_TRANSFORMED_IMAGE_SOURCE_OPTIONS, D2D1_TRANSFORMED_IMAGE_SOURCE_OPTIONS enumeration [Direct2D], D2D1_TRANSFORMED_IMAGE_SOURCE_OPTIONS_DISABLE_DPI_SCALE, D2D1_TRANSFORMED_IMAGE_SOURCE_OPTIONS_NONE, d2d1_3/D2D1_TRANSFORMED_IMAGE_SOURCE_OPTIONS, d2d1_3/D2D1_TRANSFORMED_IMAGE_SOURCE_OPTIONS_DISABLE_DPI_SCALE, d2d1_3/D2D1_TRANSFORMED_IMAGE_SOURCE_OPTIONS_NONE, direct2d.d2d1_transformed_image_source_options
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
targetos: Windows
req.typenames: D2D1_TRANSFORMED_IMAGE_SOURCE_OPTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_TRANSFORMED_IMAGE_SOURCE_OPTIONS
 - d2d1_3/D2D1_TRANSFORMED_IMAGE_SOURCE_OPTIONS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1_3.h
api_name:
 - D2D1_TRANSFORMED_IMAGE_SOURCE_OPTIONS
---

# D2D1_TRANSFORMED_IMAGE_SOURCE_OPTIONS enumeration


## -description

Option flags for transformed image sources.

## -enum-fields

### -field D2D1_TRANSFORMED_IMAGE_SOURCE_OPTIONS_NONE:0

No option flags.

### -field D2D1_TRANSFORMED_IMAGE_SOURCE_OPTIONS_DISABLE_DPI_SCALE:1

Prevents the image source from being automatically scaled (by a ratio of the context DPI divided by 96) while drawn.

### -field D2D1_TRANSFORMED_IMAGE_SOURCE_OPTIONS_FORCE_DWORD:0xffffffff

