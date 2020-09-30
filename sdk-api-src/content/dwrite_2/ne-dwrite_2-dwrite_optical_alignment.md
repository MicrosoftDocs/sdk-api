---
UID: NE:dwrite_2.DWRITE_OPTICAL_ALIGNMENT
title: DWRITE_OPTICAL_ALIGNMENT (dwrite_2.h)
description: The optical margin alignment mode.
helpviewer_keywords: ["DWRITE_OPTICAL_ALIGNMENT","DWRITE_OPTICAL_ALIGNMENT enumeration [Direct Write]","DWRITE_OPTICAL_ALIGNMENT_NONE","DWRITE_OPTICAL_ALIGNMENT_NO_SIDE_BEARINGS","directwrite.dwrite_optical_alignment","dwrite_2/DWRITE_OPTICAL_ALIGNMENT","dwrite_2/DWRITE_OPTICAL_ALIGNMENT_NONE","dwrite_2/DWRITE_OPTICAL_ALIGNMENT_NO_SIDE_BEARINGS"]
old-location: directwrite\dwrite_optical_alignment.htm
tech.root: DirectWrite
ms.assetid: 2EB04686-970A-4D79-BFF7-9AE8396A07BB
ms.date: 12/05/2018
ms.keywords: DWRITE_OPTICAL_ALIGNMENT, DWRITE_OPTICAL_ALIGNMENT enumeration [Direct Write], DWRITE_OPTICAL_ALIGNMENT_NONE, DWRITE_OPTICAL_ALIGNMENT_NO_SIDE_BEARINGS, directwrite.dwrite_optical_alignment, dwrite_2/DWRITE_OPTICAL_ALIGNMENT, dwrite_2/DWRITE_OPTICAL_ALIGNMENT_NONE, dwrite_2/DWRITE_OPTICAL_ALIGNMENT_NO_SIDE_BEARINGS
req.header: dwrite_2.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DWRITE_OPTICAL_ALIGNMENT
 - dwrite_2/DWRITE_OPTICAL_ALIGNMENT
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
 - DWRITE_OPTICAL_ALIGNMENT
---

# DWRITE_OPTICAL_ALIGNMENT enumeration


## -description

The optical margin alignment mode.

By default, glyphs are aligned to the margin by the default origin and side-bearings of the glyph. 
        If you specify <b>DWRITE_OPTICAL_ALIGNMENT_NO_SIDE_BEARINGS</b>, then the alignment uses the side bearings to offset the glyph 
        from the aligned edge to ensure the ink of the glyphs are aligned.

## -enum-fields

### -field DWRITE_OPTICAL_ALIGNMENT_NONE

Align to the default origin and side-bearings of the glyph.

### -field DWRITE_OPTICAL_ALIGNMENT_NO_SIDE_BEARINGS

Align to the ink of the glyphs, such that the black box abuts the margins.

