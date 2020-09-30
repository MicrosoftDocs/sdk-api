---
UID: NS:strmif._VMRFrequency
title: VMRFrequency (strmif.h)
description: The VMRFrequency structure describes the frequency of a video stream. Frequencies are described as ratios. For example, the NTSC frame rate of 29.97 fps is expressed as 30,000:1001.
helpviewer_keywords: ["VMRFrequency","VMRFrequency structure [DirectShow]","VMRFrequencyStructure","dshow.vmrfrequency","strmif/VMRFrequency"]
old-location: dshow\vmrfrequency.htm
tech.root: dshow
ms.assetid: fb4c094a-2760-45b2-b494-a44d5493987f
ms.date: 12/05/2018
ms.keywords: VMRFrequency, VMRFrequency structure [DirectShow], VMRFrequencyStructure, dshow.vmrfrequency, strmif/VMRFrequency
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
req.typenames: VMRFrequency
req.redist: 
req.product: Windows XP with SP1 and later
ms.custom: 19H1
f1_keywords:
 - _VMRFrequency
 - strmif/_VMRFrequency
 - VMRFrequency
 - strmif/VMRFrequency
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
 - VMRFrequency
---

# VMRFrequency structure


## -description

The <code>VMRFrequency</code> structure describes the frequency of a video stream. Frequencies are described as ratios. For example, the NTSC frame rate of 29.97 fps is expressed as 30,000:1001.

## -struct-fields

### -field dwNumerator

Numerator of the frequency ratio.

### -field dwDenominator

Denominator of the frequency ratio.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>