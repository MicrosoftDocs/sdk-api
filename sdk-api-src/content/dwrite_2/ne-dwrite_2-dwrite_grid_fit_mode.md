---
UID: NE:dwrite_2.DWRITE_GRID_FIT_MODE
title: DWRITE_GRID_FIT_MODE (dwrite_2.h)
description: Specifies whether to enable grid-fitting of glyph outlines (also known as hinting).
helpviewer_keywords: ["DWRITE_GRID_FIT_MODE","DWRITE_GRID_FIT_MODE enumeration [Direct Write]","DWRITE_GRID_FIT_MODE_DEFAULT","DWRITE_GRID_FIT_MODE_DISABLED","DWRITE_GRID_FIT_MODE_ENABLED","directwrite.dwrite_grid_fit_mode","dwrite_2/DWRITE_GRID_FIT_MODE","dwrite_2/DWRITE_GRID_FIT_MODE_DEFAULT","dwrite_2/DWRITE_GRID_FIT_MODE_DISABLED","dwrite_2/DWRITE_GRID_FIT_MODE_ENABLED"]
old-location: directwrite\dwrite_grid_fit_mode.htm
tech.root: DirectWrite
ms.assetid: C32A6017-3711-482B-B806-79651163DEF6
ms.date: 12/05/2018
ms.keywords: DWRITE_GRID_FIT_MODE, DWRITE_GRID_FIT_MODE enumeration [Direct Write], DWRITE_GRID_FIT_MODE_DEFAULT, DWRITE_GRID_FIT_MODE_DISABLED, DWRITE_GRID_FIT_MODE_ENABLED, directwrite.dwrite_grid_fit_mode, dwrite_2/DWRITE_GRID_FIT_MODE, dwrite_2/DWRITE_GRID_FIT_MODE_DEFAULT, dwrite_2/DWRITE_GRID_FIT_MODE_DISABLED, dwrite_2/DWRITE_GRID_FIT_MODE_ENABLED
req.header: dwrite_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DWRITE_GRID_FIT_MODE
 - dwrite_2/DWRITE_GRID_FIT_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dwrite_2.h
api_name:
 - DWRITE_GRID_FIT_MODE
---

# DWRITE_GRID_FIT_MODE enumeration


## -description

Specifies whether to enable grid-fitting of glyph outlines (also known as hinting).

## -enum-fields

### -field DWRITE_GRID_FIT_MODE_DEFAULT

Choose grid fitting based on the font's table information.

### -field DWRITE_GRID_FIT_MODE_DISABLED

Always disable grid fitting, using the ideal glyph outlines.

### -field DWRITE_GRID_FIT_MODE_ENABLED

Enable grid fitting, adjusting glyph outlines for device pixel display.

