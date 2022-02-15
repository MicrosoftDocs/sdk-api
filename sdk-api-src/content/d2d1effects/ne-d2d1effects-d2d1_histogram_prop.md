---
UID: NE:d2d1effects.D2D1_HISTOGRAM_PROP
title: D2D1_HISTOGRAM_PROP (d2d1effects.h)
description: Identifiers for properties of the Histogram effect.
helpviewer_keywords: ["D2D1_HISTOGRAM_PROP","D2D1_HISTOGRAM_PROP enumeration [Direct2D]","D2D1_HISTOGRAM_PROP_CHANNEL_SELECT","D2D1_HISTOGRAM_PROP_HISTOGRAM_OUTPUT","D2D1_HISTOGRAM_PROP_NUM_BINS","d2d1effects/D2D1_HISTOGRAM_PROP","d2d1effects/D2D1_HISTOGRAM_PROP_CHANNEL_SELECT","d2d1effects/D2D1_HISTOGRAM_PROP_HISTOGRAM_OUTPUT","d2d1effects/D2D1_HISTOGRAM_PROP_NUM_BINS","direct2d.d2d1_histogram_prop"]
old-location: direct2d\d2d1_histogram_prop.htm
tech.root: Direct2D
ms.assetid: 7CBF945C-3BBA-4243-A76B-5CDAC045E79C
ms.date: 12/05/2018
ms.keywords: D2D1_HISTOGRAM_PROP, D2D1_HISTOGRAM_PROP enumeration [Direct2D], D2D1_HISTOGRAM_PROP_CHANNEL_SELECT, D2D1_HISTOGRAM_PROP_HISTOGRAM_OUTPUT, D2D1_HISTOGRAM_PROP_NUM_BINS, d2d1effects/D2D1_HISTOGRAM_PROP, d2d1effects/D2D1_HISTOGRAM_PROP_CHANNEL_SELECT, d2d1effects/D2D1_HISTOGRAM_PROP_HISTOGRAM_OUTPUT, d2d1effects/D2D1_HISTOGRAM_PROP_NUM_BINS, direct2d.d2d1_histogram_prop
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
req.typenames: D2D1_HISTOGRAM_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_HISTOGRAM_PROP
 - d2d1effects/D2D1_HISTOGRAM_PROP
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
 - D2D1_HISTOGRAM_PROP
---

# D2D1_HISTOGRAM_PROP enumeration


## -description

Identifiers for properties of the <a href="/windows/desktop/Direct2D/histogram">Histogram effect</a>.

## -enum-fields

### -field D2D1_HISTOGRAM_PROP_NUM_BINS:0

Specifies the number of bins used for the histogram. The range of intensity values that fall into a particular bucket depend on the number of specified buckets. 
          

The type is UINT32.

The default is 256.

### -field D2D1_HISTOGRAM_PROP_CHANNEL_SELECT:1

Specifies the channel used to generate the histogram. This effect has a single data output corresponding to the specified channel.
          

The type is <a href="/windows/desktop/api/d2d1effects/ne-d2d1effects-d2d1_channel_selector">D2D1_CHANNEL_SELECTOR</a>.

The default is D2D1_CHANNEL_SELECTOR_R.

### -field D2D1_HISTOGRAM_PROP_HISTOGRAM_OUTPUT:2

The output array.
          

The type is FLOAT[].

### -field D2D1_HISTOGRAM_PROP_FORCE_DWORD:0xffffffff
