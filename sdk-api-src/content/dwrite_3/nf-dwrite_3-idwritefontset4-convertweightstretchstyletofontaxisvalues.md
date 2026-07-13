---
UID: NF:dwrite_3.IDWriteFontSet4.ConvertWeightStretchStyleToFontAxisValues
tech.root: DirectWrite
title: IDWriteFontSet4::ConvertWeightStretchStyleToFontAxisValues
ms.date: 09/10/2025
targetos: Windows
description: Computes derived font axis values from the specified font weight, stretch, style, and size.
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
 - IDWriteFontSet4::ConvertWeightStretchStyleToFontAxisValues
f1_keywords:
 - IDWriteFontSet4::ConvertWeightStretchStyleToFontAxisValues
 - dwrite_3/IDWriteFontSet4::ConvertWeightStretchStyleToFontAxisValues
dev_langs:
 - c++
helpviewer_keywords:
 - ConvertWeightStretchStyleToFontAxisValues
prerelease: false
---

## -description

Computes derived font axis values from the specified font weight, stretch, style, and size.

## -parameters

### -param inputAxisValues

Type: \_In\_reads\_opt\_(inputAxisCount) **[DWRITE_FONT_AXIS_VALUE](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_value) const\***

Optional pointer to an array of input axis values. Axes present in this array are excluded from the output. That's so that explicit axis values take precedence over derived axis values.

### -param inputAxisCount

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

Size of the array of input axis values.

### -param fontWeight

Type: **[DWRITE_FONT_WEIGHT](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight)**

Font weight, used to compute "wght" axis value.

### -param fontStretch

Type: **[DWRITE_FONT_STRETCH](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch)**

Font stretch, used to compute "wdth" axis value.

### -param fontStyle

Type: **[DWRITE_FONT_STYLE](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style)**

Font style, used to compute "slnt" and "ital" axis values.

### -param fontSize

Type: **float**

Font size in DIPs, used to compute "opsz" axis value. If this parameter is zero, then no "opsz" axis value is added to the output array.

### -param outputAxisValues

Type: \_Out\_writes\_to\_(DWRITE_STANDARD_FONT_AXIS_COUNT, return) **[DWRITE_FONT_AXIS_VALUE](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_value)\***

Pointer to an output array to which derived axis values are written. The size of this array must be at least **DWRITE_STANDARD_FONT_AXIS_COUNT** (5). The return value is the number of axis values that were actually written to this array.

## -returns

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

Returns the number of derived axis values that were actually written to the output array.

## -remarks

The caller should concatenate the output axis values to the input axis values (if any), and pass the combined axis values to the **GetMatchingFonts** method. This doesn't result in duplicates because the output doesn't include any axes present in the *inputAxisValues* array.

## -see-also
