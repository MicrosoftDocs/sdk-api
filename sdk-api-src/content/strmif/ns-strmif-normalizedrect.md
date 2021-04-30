---
UID: NS:strmif._NORMALIZEDRECT
title: NORMALIZEDRECT (strmif.h)
description: The NORMALIZEDRECT structure is used with the VMR filter in mixing operations to specify the location of a video rectangle in composition space.
helpviewer_keywords: ["*PNORMALIZEDRECT","NORMALIZEDRECT","NORMALIZEDRECT structure [DirectShow]","NORMALIZEDRECT2","PNORMALIZEDRECT","PNORMALIZEDRECT structure pointer [DirectShow]","dshow.normalizedrect","strmif/NORMALIZEDRECT","strmif/PNORMALIZEDRECT"]
old-location: dshow\normalizedrect.htm
tech.root: dshow
ms.assetid: c40a0feb-f33e-40e3-9c58-0a22d2aa1858
ms.date: 12/05/2018
ms.keywords: '*PNORMALIZEDRECT, NORMALIZEDRECT, NORMALIZEDRECT structure [DirectShow], NORMALIZEDRECT2, PNORMALIZEDRECT, PNORMALIZEDRECT structure pointer [DirectShow], dshow.normalizedrect, strmif/NORMALIZEDRECT, strmif/PNORMALIZEDRECT'
req.header: strmif.h
req.include-header: Dshow.h
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
req.typenames: NORMALIZEDRECT, *PNORMALIZEDRECT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NORMALIZEDRECT
 - strmif/_NORMALIZEDRECT
 - PNORMALIZEDRECT
 - strmif/PNORMALIZEDRECT
 - NORMALIZEDRECT
 - strmif/NORMALIZEDRECT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - NORMALIZEDRECT
---

# NORMALIZEDRECT structure


## -description

The <code>NORMALIZEDRECT</code> structure is used with the VMR filter in mixing operations to specify the location of a video rectangle in composition space.

## -struct-fields

### -field left

The left corner of the normalized rectangle.

### -field top

The top corner of the normalized rectangle.

### -field right

The right corner of the normalized rectangle.

### -field bottom

The bottom corner of the normalized rectangle.

## -remarks

This structure is used in methods involving "composition space," which refers to the visible video rectangle, as well as the offscreen space necessary to contain rectangles from secondary streams. See <a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a> for more information.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>