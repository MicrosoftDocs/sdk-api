---
UID: NE:dcommon.DWRITE_MEASURING_MODE
title: DWRITE_MEASURING_MODE (dcommon.h)
description: Indicates the measuring method used for text layout.
helpviewer_keywords: ["DWRITE_MEASURING_MODE","DWRITE_MEASURING_MODE enumeration [Direct Write]","DWRITE_MEASURING_MODE_GDI_CLASSIC","DWRITE_MEASURING_MODE_GDI_NATURAL","DWRITE_MEASURING_MODE_NATURAL","dcommon/DWRITE_MEASURING_MODE","dcommon/DWRITE_MEASURING_MODE_GDI_CLASSIC","dcommon/DWRITE_MEASURING_MODE_GDI_NATURAL","dcommon/DWRITE_MEASURING_MODE_NATURAL","directwrite.dwrite_text_measuring_method"]
old-location: directwrite\dwrite_text_measuring_method.htm
tech.root: DirectWrite
ms.assetid: 99e89754-8bc2-457d-bfdb-a3c9ccfe00c1
ms.date: 12/05/2018
ms.keywords: DWRITE_MEASURING_MODE, DWRITE_MEASURING_MODE enumeration [Direct Write], DWRITE_MEASURING_MODE_GDI_CLASSIC, DWRITE_MEASURING_MODE_GDI_NATURAL, DWRITE_MEASURING_MODE_NATURAL, dcommon/DWRITE_MEASURING_MODE, dcommon/DWRITE_MEASURING_MODE_GDI_CLASSIC, dcommon/DWRITE_MEASURING_MODE_GDI_NATURAL, dcommon/DWRITE_MEASURING_MODE_NATURAL, directwrite.dwrite_text_measuring_method
req.header: dcommon.h
req.include-header: Dwrite.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: DWRITE_MEASURING_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DWRITE_MEASURING_MODE
 - dcommon/DWRITE_MEASURING_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dcommon.h
api_name:
 - DWRITE_MEASURING_MODE
---

# DWRITE_MEASURING_MODE enumeration


## -description

Indicates the measuring method used for text layout.

## -enum-fields

### -field DWRITE_MEASURING_MODE_NATURAL

Specifies that text is measured using glyph ideal metrics whose values are independent to the current display resolution.

### -field DWRITE_MEASURING_MODE_GDI_CLASSIC

Specifies that text is measured using glyph display-compatible metrics whose values tuned for the current display resolution.

### -field DWRITE_MEASURING_MODE_GDI_NATURAL

Specifies that text is measured using the same glyph display metrics as text measured by GDI using a font created with CLEARTYPE_NATURAL_QUALITY.

