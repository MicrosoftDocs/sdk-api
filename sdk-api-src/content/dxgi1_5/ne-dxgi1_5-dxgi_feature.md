---
UID: NE:dxgi1_5.DXGI_FEATURE
title: DXGI_FEATURE (dxgi1_5.h)
description: Specifies a range of hardware features, to be used when checking for feature support.
helpviewer_keywords: ["DXGI_FEATURE","DXGI_FEATURE enumeration [DXGI]","DXGI_FEATURE_PRESENT_ALLOW_TEARING","direct3ddxgi.dxgi_feature","dxgi1_5/DXGI_FEATURE","dxgi1_5/DXGI_FEATURE_PRESENT_ALLOW_TEARING"]
old-location: direct3ddxgi\dxgi_feature.htm
tech.root: direct3ddxgi
ms.assetid: 207D5BDC-5D10-4F84-931F-4812574FA74B
ms.date: 12/05/2018
ms.keywords: DXGI_FEATURE, DXGI_FEATURE enumeration [DXGI], DXGI_FEATURE_PRESENT_ALLOW_TEARING, direct3ddxgi.dxgi_feature, dxgi1_5/DXGI_FEATURE, dxgi1_5/DXGI_FEATURE_PRESENT_ALLOW_TEARING
req.header: dxgi1_5.h
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
req.typenames: DXGI_FEATURE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGI_FEATURE
 - dxgi1_5/DXGI_FEATURE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DXGI1_5.h
api_name:
 - DXGI_FEATURE
---

# DXGI_FEATURE enumeration


## -description

Specifies a range of hardware features, to be used when checking for feature support.

## -enum-fields

### -field DXGI_FEATURE_PRESENT_ALLOW_TEARING:0

The display supports tearing, a requirement of variable refresh rate displays.

## -remarks

This enum is used by the <a href="/windows/desktop/api/dxgi1_5/nf-dxgi1_5-idxgifactory5-checkfeaturesupport">CheckFeatureSupport</a> method.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-enums">DXGI Enumerations</a>
