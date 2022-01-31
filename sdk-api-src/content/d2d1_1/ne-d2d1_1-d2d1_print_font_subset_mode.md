---
UID: NE:d2d1_1.D2D1_PRINT_FONT_SUBSET_MODE
title: D2D1_PRINT_FONT_SUBSET_MODE (d2d1_1.h)
description: Defines when font resources should be subset during printing.
helpviewer_keywords: ["D2D1_PRINT_FONT_SUBSET_DEFAULT","D2D1_PRINT_FONT_SUBSET_EACHPAGE","D2D1_PRINT_FONT_SUBSET_MODE","D2D1_PRINT_FONT_SUBSET_MODE enumeration [Direct2D]","D2D1_PRINT_FONT_SUBSET_NONE","d2d1_1/D2D1_PRINT_FONT_SUBSET_DEFAULT","d2d1_1/D2D1_PRINT_FONT_SUBSET_EACHPAGE","d2d1_1/D2D1_PRINT_FONT_SUBSET_MODE","d2d1_1/D2D1_PRINT_FONT_SUBSET_NONE","direct2d.d2d1_cprint_font_subset_mode"]
old-location: direct2d\d2d1_cprint_font_subset_mode.htm
tech.root: Direct2D
ms.assetid: B8361117-6018-48EE-AD3D-2A37F6B71293
ms.date: 12/05/2018
ms.keywords: D2D1_PRINT_FONT_SUBSET_DEFAULT, D2D1_PRINT_FONT_SUBSET_EACHPAGE, D2D1_PRINT_FONT_SUBSET_MODE, D2D1_PRINT_FONT_SUBSET_MODE enumeration [Direct2D], D2D1_PRINT_FONT_SUBSET_NONE, d2d1_1/D2D1_PRINT_FONT_SUBSET_DEFAULT, d2d1_1/D2D1_PRINT_FONT_SUBSET_EACHPAGE, d2d1_1/D2D1_PRINT_FONT_SUBSET_MODE, d2d1_1/D2D1_PRINT_FONT_SUBSET_NONE, direct2d.d2d1_cprint_font_subset_mode
req.header: d2d1_1.h
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
req.typenames: D2D1_PRINT_FONT_SUBSET_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_PRINT_FONT_SUBSET_MODE
 - d2d1_1/D2D1_PRINT_FONT_SUBSET_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1_1.h
api_name:
 - D2D1_PRINT_FONT_SUBSET_MODE
---

## -description

Defines when font resources should be subset during printing.

## -enum-fields

### -field D2D1_PRINT_FONT_SUBSET_MODE_DEFAULT:0

Uses a heuristic strategy to decide when to subset fonts. 

> [!NOTE]
> If the print driver has requested archive-optimized content, then Direct2D will subset fonts once, for the entire document.

### -field D2D1_PRINT_FONT_SUBSET_MODE_EACHPAGE:1

Subsets and embeds font resources in each page, then discards that font subset after the page is printed out.

### -field D2D1_PRINT_FONT_SUBSET_MODE_NONE:2

Sends out the original font resources without subsetting along with the page that first uses the font, and re-uses the font resources for later pages without resending them.

### -field D2D1_PRINT_FONT_SUBSET_MODE_FORCE_DWORD:0xffffffff

A value that's guaranteed to be a DWORD.

## -see-also

<a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_print_control_properties">D2D1_PRINT_CONTROL_PROPERTIES</a>
