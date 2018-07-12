---
UID: NF:mileffects.IMILBitmapEffectPrimitive.TransformPoint
title: IMILBitmapEffectPrimitive::TransformPoint
author: windows-sdk-content
description: Transforms the given point.
old-location: wibe\_wibe_imilbitmapeffectprimitive_transformpoint.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectprimitive\transformpoint.htm
ms.author: windowssdkdev
ms.date: 06/14/2018
ms.keywords: IMILBitmapEffectPrimitive interface [WPF Bitmap Effects],TransformPoint method, IMILBitmapEffectPrimitive.TransformPoint, IMILBitmapEffectPrimitive::TransformPoint, TransformPoint, TransformPoint method [WPF Bitmap Effects], TransformPoint method [WPF Bitmap Effects],IMILBitmapEffectPrimitive interface, _wibe_imilbitmapeffectprimitive_transformpoint, mileffects/IMILBitmapEffectPrimitive::TransformPoint, wibe._wibe_imilbitmapeffectprimitive_transformpoint
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: MICUIELEMENTSTATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mileffects.h
api_name:
 - IMILBitmapEffectPrimitive.TransformPoint
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMILBitmapEffectPrimitive::TransformPoint


## -description


Transforms the given point.


## -parameters




### -param uiIndex [in]

Type: <b>ULONG</b>

A zero based index value indicating the output pin through which to transform the point.


### -param p [in, out]

Type: <b><a href="https://msdn.microsoft.com/library/ms735226(v=VS.85).aspx">MIL_2DPOINTD</a>*</b>

A pointer to the point to transform.


### -param fForwardTransform [in]

Type: <b>VARIANT_BOOL</b>

A value indicating whether the point is being transformed from front to back in the effects graph.


### -param pContext [in]

Type: <b><a href="https://msdn.microsoft.com/library/ms735245(v=VS.85).aspx">IMILBitmapEffectRenderContext</a>*</b>

The render context to use for the transformation.


### -param pfPointTransformed [out]

Type: <b>VARIANT_BOOL*</b>

When this method returns, contains a value indicating whether the point transformed to a known location.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



