---
UID: NF:mileffects.IMILBitmapEffectPrimitive.GetAffineMatrix
title: IMILBitmapEffectPrimitive::GetAffineMatrix
author: windows-sdk-content
description: Retrieves the affine transormation matrix for the effect.
old-location: wibe\_wibe_imilbitmapeffectprimitive_getaffinematrix.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectprimitive\getaffinematrix.htm
ms.author: windowssdkdev
ms.date: 06/14/2018
ms.keywords: GetAffineMatrix, GetAffineMatrix method [WPF Bitmap Effects], GetAffineMatrix method [WPF Bitmap Effects],IMILBitmapEffectPrimitive interface, IMILBitmapEffectPrimitive interface [WPF Bitmap Effects],GetAffineMatrix method, IMILBitmapEffectPrimitive.GetAffineMatrix, IMILBitmapEffectPrimitive::GetAffineMatrix, _wibe_imilbitmapeffectprimitive_getaffinematrix, mileffects/IMILBitmapEffectPrimitive::GetAffineMatrix, wibe._wibe_imilbitmapeffectprimitive_getaffinematrix
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
 - IMILBitmapEffectPrimitive.GetAffineMatrix
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMILBitmapEffectPrimitive::GetAffineMatrix


## -description


Retrieves the affine transormation matrix for the effect.


## -parameters




### -param uiIndex [in]

Type: <b>ULONG</b>

A zero based index value indicating the output pin through which to retrieve the affine matrix.


### -param pMatrix [in, out]

Type: <b><a href="https://msdn.microsoft.com/ab98ba80-da72-462c-b774-304b257b2a7d">MIL_MATRIX3X2D</a>*</b>

When this method returns, contains a pointer to the affine matrix describing the effects transform.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



