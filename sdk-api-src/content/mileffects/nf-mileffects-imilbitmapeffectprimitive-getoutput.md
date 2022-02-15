---
UID: NF:mileffects.IMILBitmapEffectPrimitive.GetOutput
title: IMILBitmapEffectPrimitive::GetOutput (mileffects.h)
description: Performs pixel processing for the bitmap effect.
helpviewer_keywords: ["GetOutput","GetOutput method [WPF Bitmap Effects]","GetOutput method [WPF Bitmap Effects]","IMILBitmapEffectPrimitive interface","IMILBitmapEffectPrimitive interface [WPF Bitmap Effects]","GetOutput method","IMILBitmapEffectPrimitive.GetOutput","IMILBitmapEffectPrimitive::GetOutput","_wibe_imilbitmapeffectprimitive_getoutput","mileffects/IMILBitmapEffectPrimitive::GetOutput","wibe._wibe_imilbitmapeffectprimitive_getoutput"]
old-location: wibe\_wibe_imilbitmapeffectprimitive_getoutput.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectprimitive\getoutput.htm
ms.date: 12/05/2018
ms.keywords: GetOutput, GetOutput method [WPF Bitmap Effects], GetOutput method [WPF Bitmap Effects],IMILBitmapEffectPrimitive interface, IMILBitmapEffectPrimitive interface [WPF Bitmap Effects],GetOutput method, IMILBitmapEffectPrimitive.GetOutput, IMILBitmapEffectPrimitive::GetOutput, _wibe_imilbitmapeffectprimitive_getoutput, mileffects/IMILBitmapEffectPrimitive::GetOutput, wibe._wibe_imilbitmapeffectprimitive_getoutput
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
 - IMILBitmapEffectPrimitive::GetOutput
 - mileffects/IMILBitmapEffectPrimitive::GetOutput
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
 - IMILBitmapEffectPrimitive.GetOutput
---

# IMILBitmapEffectPrimitive::GetOutput


## -description

Performs pixel processing for the bitmap effect.

## -parameters

### -param uiIndex [in]

Type: <b>ULONG</b>

A zero based index value indicating which output pin to use for output.

### -param pContext [in]

Type: <b><a href="/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectrendercontext">IMILBitmapEffectRenderContext</a>*</b>

The render context to use to determine how the effect should be rendered.

### -param pfModifyInPlace [in, out]

Type: <b>VARIANT_BOOL*</b>

A value that indicates whether the effect should attempt to modify the input image in place.

### -param ppBitmapSource [out, retval]

Type: <b>IWICBitmapSource**</b>

When this method returns, contains a pointer to the effect output.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If <i>pfModifyInPlace</i> is VARIANT_TRUE, the input image may be modified and returned.
            If the custom effect does not support in place modifications, set <i>pfModifyInPlace</i> to VARIANT_FALSE to indicate a new image was created.