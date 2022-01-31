---
UID: NE:d2d1_1.D2D1_COMPOSITE_MODE
title: D2D1_COMPOSITE_MODE (d2d1_1.h)
description: Used to specify the blend mode for all of the Direct2D blending operations.
helpviewer_keywords: ["D2D1_COMPOSITE_MODE","D2D1_COMPOSITE_MODE enumeration [Direct2D]","D2D1_COMPOSITE_MODE_BOUNDED_SOURCE_COPY","D2D1_COMPOSITE_MODE_DESTINATION_ATOP","D2D1_COMPOSITE_MODE_DESTINATION_IN","D2D1_COMPOSITE_MODE_DESTINATION_OUT","D2D1_COMPOSITE_MODE_DESTINATION_OVER","D2D1_COMPOSITE_MODE_MASK_INVERT","D2D1_COMPOSITE_MODE_PLUS","D2D1_COMPOSITE_MODE_SOURCE_ATOP","D2D1_COMPOSITE_MODE_SOURCE_COPY","D2D1_COMPOSITE_MODE_SOURCE_IN","D2D1_COMPOSITE_MODE_SOURCE_OUT","D2D1_COMPOSITE_MODE_SOURCE_OVER","D2D1_COMPOSITE_MODE_XOR","d2d1_1/D2D1_COMPOSITE_MODE","d2d1_1/D2D1_COMPOSITE_MODE_BOUNDED_SOURCE_COPY","d2d1_1/D2D1_COMPOSITE_MODE_DESTINATION_ATOP","d2d1_1/D2D1_COMPOSITE_MODE_DESTINATION_IN","d2d1_1/D2D1_COMPOSITE_MODE_DESTINATION_OUT","d2d1_1/D2D1_COMPOSITE_MODE_DESTINATION_OVER","d2d1_1/D2D1_COMPOSITE_MODE_MASK_INVERT","d2d1_1/D2D1_COMPOSITE_MODE_PLUS","d2d1_1/D2D1_COMPOSITE_MODE_SOURCE_ATOP","d2d1_1/D2D1_COMPOSITE_MODE_SOURCE_COPY","d2d1_1/D2D1_COMPOSITE_MODE_SOURCE_IN","d2d1_1/D2D1_COMPOSITE_MODE_SOURCE_OUT","d2d1_1/D2D1_COMPOSITE_MODE_SOURCE_OVER","d2d1_1/D2D1_COMPOSITE_MODE_XOR","direct2d.__d2d1_composite_mode"]
old-location: direct2d\__d2d1_composite_mode.htm
tech.root: Direct2D
ms.assetid: 4f01e805-aed7-4bfc-9793-42a9fdde3473
ms.date: 12/05/2018
ms.keywords: D2D1_COMPOSITE_MODE, D2D1_COMPOSITE_MODE enumeration [Direct2D], D2D1_COMPOSITE_MODE_BOUNDED_SOURCE_COPY, D2D1_COMPOSITE_MODE_DESTINATION_ATOP, D2D1_COMPOSITE_MODE_DESTINATION_IN, D2D1_COMPOSITE_MODE_DESTINATION_OUT, D2D1_COMPOSITE_MODE_DESTINATION_OVER, D2D1_COMPOSITE_MODE_MASK_INVERT, D2D1_COMPOSITE_MODE_PLUS, D2D1_COMPOSITE_MODE_SOURCE_ATOP, D2D1_COMPOSITE_MODE_SOURCE_COPY, D2D1_COMPOSITE_MODE_SOURCE_IN, D2D1_COMPOSITE_MODE_SOURCE_OUT, D2D1_COMPOSITE_MODE_SOURCE_OVER, D2D1_COMPOSITE_MODE_XOR, d2d1_1/D2D1_COMPOSITE_MODE, d2d1_1/D2D1_COMPOSITE_MODE_BOUNDED_SOURCE_COPY, d2d1_1/D2D1_COMPOSITE_MODE_DESTINATION_ATOP, d2d1_1/D2D1_COMPOSITE_MODE_DESTINATION_IN, d2d1_1/D2D1_COMPOSITE_MODE_DESTINATION_OUT, d2d1_1/D2D1_COMPOSITE_MODE_DESTINATION_OVER, d2d1_1/D2D1_COMPOSITE_MODE_MASK_INVERT, d2d1_1/D2D1_COMPOSITE_MODE_PLUS, d2d1_1/D2D1_COMPOSITE_MODE_SOURCE_ATOP, d2d1_1/D2D1_COMPOSITE_MODE_SOURCE_COPY, d2d1_1/D2D1_COMPOSITE_MODE_SOURCE_IN, d2d1_1/D2D1_COMPOSITE_MODE_SOURCE_OUT, d2d1_1/D2D1_COMPOSITE_MODE_SOURCE_OVER, d2d1_1/D2D1_COMPOSITE_MODE_XOR, direct2d.__d2d1_composite_mode
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: D2D1_COMPOSITE_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_COMPOSITE_MODE
 - d2d1_1/D2D1_COMPOSITE_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D2d1_1.h
api_name:
 - D2D1_COMPOSITE_MODE
---

## -description

Used to specify the blend mode for all of the Direct2D blending operations.

## -enum-fields

### -field D2D1_COMPOSITE_MODE_SOURCE_OVER:0

The standard source-over-destination blend mode.

### -field D2D1_COMPOSITE_MODE_DESTINATION_OVER:1

The destination is rendered over the source.

### -field D2D1_COMPOSITE_MODE_SOURCE_IN:2

Performs a logical clip of the source pixels against the destination pixels.

### -field D2D1_COMPOSITE_MODE_DESTINATION_IN:3

The inverse of the <b>D2D1_COMPOSITE_MODE_SOURCE_IN</b> operation.

### -field D2D1_COMPOSITE_MODE_SOURCE_OUT:4

This is the logical inverse to <b>D2D1_COMPOSITE_MODE_SOURCE_IN</b>.

### -field D2D1_COMPOSITE_MODE_DESTINATION_OUT:5

The is the logical inverse to <b>D2D1_COMPOSITE_MODE_DESTINATION_IN</b>.

### -field D2D1_COMPOSITE_MODE_SOURCE_ATOP:6

Writes the source pixels over the destination where there are destination pixels.

### -field D2D1_COMPOSITE_MODE_DESTINATION_ATOP:7

The logical inverse of <b>D2D1_COMPOSITE_MODE_SOURCE_ATOP</b>.

### -field D2D1_COMPOSITE_MODE_XOR:8

The source is inverted with the destination.

### -field D2D1_COMPOSITE_MODE_PLUS:9

The channel components are summed.

### -field D2D1_COMPOSITE_MODE_SOURCE_COPY:10

The source is copied to the destination; the destination pixels are ignored.

### -field D2D1_COMPOSITE_MODE_BOUNDED_SOURCE_COPY:11

Equivalent to <b>D2D1_COMPOSITE_MODE_SOURCE_COPY</b>, but pixels outside of the source bounds are unchanged.

### -field D2D1_COMPOSITE_MODE_MASK_INVERT:12

Destination colors are inverted according to a source mask.

### -field D2D1_COMPOSITE_MODE_FORCE_DWORD:0xffffffff

## -remarks

The figure here shows an example of each of the modes with images that have an opacity of 1.0 or 0.5. 

<img alt="An example image of each of the modes with opacity set to 1.0 or 0.5." src="./images/composite_types.png"/>

There can be slightly different interpretations of these enumeration values depending on where the value is used.

<ul>
<li>
With a composite effect:

<b>D2D1_COMPOSITE_MODE_DESTINATION_COPY</b> is equivalent to <b>D2D1_COMPOSITE_MODE_SOURCE_COPY</b> with the inputs inverted.</li>
<li>
As a parameter to <a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1effect_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)">ID2D1DeviceContext::DrawImage</a>: 
<b>D2D1_COMPOSITE_MODE_DESTINATION_COPY</b> is a no-op since the destination is already in the selected target.</li>
</ul>
<h3><a id="Sample_code"></a><a id="sample_code"></a><a id="SAMPLE_CODE"></a>Sample code</h3>
For an example that uses composite modes, download the <a href="https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample">Direct2D composite effect modes sample</a>.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1effect_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)">ID2D1DeviceContext::DrawImage</a>
