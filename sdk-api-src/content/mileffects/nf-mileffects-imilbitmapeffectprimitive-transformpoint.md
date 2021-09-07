---
UID: NF:mileffects.IMILBitmapEffectPrimitive.TransformPoint
title: IMILBitmapEffectPrimitive::TransformPoint (mileffects.h)
description: Transforms the given point.
helpviewer_keywords: ["IMILBitmapEffectPrimitive interface [WPF Bitmap Effects]","TransformPoint method","IMILBitmapEffectPrimitive.TransformPoint","IMILBitmapEffectPrimitive::TransformPoint","TransformPoint","TransformPoint method [WPF Bitmap Effects]","TransformPoint method [WPF Bitmap Effects]","IMILBitmapEffectPrimitive interface","_wibe_imilbitmapeffectprimitive_transformpoint","mileffects/IMILBitmapEffectPrimitive::TransformPoint","wibe._wibe_imilbitmapeffectprimitive_transformpoint"]
old-location: wibe\_wibe_imilbitmapeffectprimitive_transformpoint.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectprimitive\transformpoint.htm
ms.date: 12/05/2018
ms.keywords: IMILBitmapEffectPrimitive interface [WPF Bitmap Effects],TransformPoint method, IMILBitmapEffectPrimitive.TransformPoint, IMILBitmapEffectPrimitive::TransformPoint, TransformPoint, TransformPoint method [WPF Bitmap Effects], TransformPoint method [WPF Bitmap Effects],IMILBitmapEffectPrimitive interface, _wibe_imilbitmapeffectprimitive_transformpoint, mileffects/IMILBitmapEffectPrimitive::TransformPoint, wibe._wibe_imilbitmapeffectprimitive_transformpoint
req.header: mileffects.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mileffects.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Microsoft .Net 3.0
ms.custom: 19H1
f1_keywords:
 - IMILBitmapEffectPrimitive::TransformPoint
 - mileffects/IMILBitmapEffectPrimitive::TransformPoint
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mileffects.h
api_name:
 - IMILBitmapEffectPrimitive.TransformPoint
---

# IMILBitmapEffectPrimitive::TransformPoint


## -description

Transforms the given point.

## -parameters

### -param uiIndex [in]

Type: <b>ULONG</b>

A zero based index value indicating the output pin through which to transform the point.

### -param p [in, out]

Type: <b><a href="/previous-versions/windows/desktop/api/mileffects/ns-mileffects-milpoint2d">MIL_2DPOINTD</a>*</b>

A pointer to the point to transform.

### -param fForwardTransform [in]

Type: <b>VARIANT_BOOL</b>

A value indicating whether the point is being transformed from front to back in the effects graph.

### -param pContext [in]

Type: <b><a href="/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectrendercontext">IMILBitmapEffectRenderContext</a>*</b>

The render context to use for the transformation.

### -param pfPointTransformed [out]

Type: <b>VARIANT_BOOL*</b>

When this method returns, contains a value indicating whether the point transformed to a known location.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.