---
UID: NS:dxvahd._DXVAHD_RATIONAL
title: DXVAHD_RATIONAL (dxvahd.h)
description: Contains a rational number (ratio).
helpviewer_keywords: ["DXVAHD_RATIONAL","DXVAHD_RATIONAL structure [Media Foundation]","dxvahd/DXVAHD_RATIONAL","mf.dxvahd_rational"]
old-location: mf\dxvahd_rational.htm
tech.root: mf
ms.assetid: 8064820e-533e-4b40-8eeb-e3ad6a6b1ff7
ms.date: 12/05/2018
ms.keywords: DXVAHD_RATIONAL, DXVAHD_RATIONAL structure [Media Foundation], dxvahd/DXVAHD_RATIONAL, mf.dxvahd_rational
req.header: dxvahd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: DXVAHD_RATIONAL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVAHD_RATIONAL
 - dxvahd/_DXVAHD_RATIONAL
 - DXVAHD_RATIONAL
 - dxvahd/DXVAHD_RATIONAL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxvahd.h
api_name:
 - DXVAHD_RATIONAL
---

# DXVAHD_RATIONAL structure


## -description

Contains a rational number (ratio).

## -struct-fields

### -field Numerator

The numerator of the ratio.

### -field Denominator

The denominator of the ratio.

## -remarks

Values of the form 0/<i>n</i> are interpreted as zero. The value 0/0 is interpreted as zero.  However, these values are not necessarily valid in all contexts.

Values of the form <i>n</i>/0, where <i>n</i> is nonzero, are invalid.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/medfound/direct3d-video-structures">Direct3D Video Structures</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>