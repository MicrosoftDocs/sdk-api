---
UID: NF:dwrite_3.IDWriteFontSet4.GetMatchingFonts
tech.root: DirectWrite
title: IDWriteFontSet4::GetMatchingFonts
ms.date: 09/10/2025
targetos: Windows
description: Generates a matching font set based on the requested inputs, ordered so that nearer matches are earlier.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Dwrite.dll
req.header: dwrite_3.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Dwrite.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11 Build 22621
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - Dwrite.dll
api_name:
 - IDWriteFontSet4::GetMatchingFonts
f1_keywords:
 - IDWriteFontSet4::GetMatchingFonts
 - dwrite_3/IDWriteFontSet4::GetMatchingFonts
dev_langs:
 - c++
helpviewer_keywords:
 - GetMatchingFonts
prerelease: false
---

## -description

Generates a matching font set based on the requested inputs, ordered so that nearer matches are earlier.

## -parameters

### -param familyName

Type: \_In\_z\_ **[WCHAR](/windows/win32/winprog/windows-data-types) const\***

Font family name. This can be: a typographic family name, weight/stretch/style family name, GDI (RBIZ) family name, or full name.

### -param fontAxisValues

Type: \_In\_reads\_(fontAxisValueCount) **[DWRITE_FONT_AXIS_VALUE](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_value) const\***

Array of font axis values.

### -param fontAxisValueCount

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

Number of font axis values.

### -param allowedSimulations

Type: **[DWRITE_FONT_SIMULATIONS](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_simulations)**

Specifies which simulations (that is, algorithmic emboldening and/or slant) may be applied to matching fonts to better match the specified axis values. If the argument is **DWRITE_FONT_SIMULATIONS_NONE** (0), then no simulations are applied.

### -param matchingFonts

Type: \_COM\_Outptr\_ **[IDWriteFontSet4](.\nn-dwrite_3-idwritefontset4.md)\*\***

Receives a pointer to a newly-created font set, which contains a prioritized list of fonts that match the specified inputs.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, then it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).

## -remarks

This can yield distinct items that were not in the original font set, including items with simulation flags (if they would be a closer match to the request) and instances that were not named by the font author. Items from the same font resources are collapsed into one: the closest possible match.

## -see-also
