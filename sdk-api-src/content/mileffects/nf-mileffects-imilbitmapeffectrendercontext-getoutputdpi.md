---
UID: NF:mileffects.IMILBitmapEffectRenderContext.GetOutputDPI
title: IMILBitmapEffectRenderContext::GetOutputDPI (mileffects.h)
description: Gets the output dots per inch (dpi).
helpviewer_keywords: ["GetOutputDPI","GetOutputDPI method [WPF Bitmap Effects]","GetOutputDPI method [WPF Bitmap Effects]","IMILBitmapEffectRenderContext interface","IMILBitmapEffectRenderContext interface [WPF Bitmap Effects]","GetOutputDPI method","IMILBitmapEffectRenderContext.GetOutputDPI","IMILBitmapEffectRenderContext::GetOutputDPI","_wibe_imilbitmapeffectrendercontext_getoutputdpi","mileffects/IMILBitmapEffectRenderContext::GetOutputDPI","wibe._wibe_imilbitmapeffectrendercontext_getoutputdpi"]
old-location: wibe\_wibe_imilbitmapeffectrendercontext_getoutputdpi.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectrendercontext\getoutputdpi.htm
ms.date: 12/05/2018
ms.keywords: GetOutputDPI, GetOutputDPI method [WPF Bitmap Effects], GetOutputDPI method [WPF Bitmap Effects],IMILBitmapEffectRenderContext interface, IMILBitmapEffectRenderContext interface [WPF Bitmap Effects],GetOutputDPI method, IMILBitmapEffectRenderContext.GetOutputDPI, IMILBitmapEffectRenderContext::GetOutputDPI, _wibe_imilbitmapeffectrendercontext_getoutputdpi, mileffects/IMILBitmapEffectRenderContext::GetOutputDPI, wibe._wibe_imilbitmapeffectrendercontext_getoutputdpi
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
req.dll: Mileffects.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Microsoft .Net 3.0
ms.custom: 19H1
f1_keywords:
 - IMILBitmapEffectRenderContext::GetOutputDPI
 - mileffects/IMILBitmapEffectRenderContext::GetOutputDPI
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mileffects.dll
api_name:
 - IMILBitmapEffectRenderContext.GetOutputDPI
---

# IMILBitmapEffectRenderContext::GetOutputDPI


## -description

Gets the output dots per inch (dpi).

## -parameters

### -param pdblDpiX [out]

Type: <b>double*</b>

A pointer that receives the horizontal resolution.

### -param pdblDpiY [out]

Type: <b>double*</b>

A pointer that receives the vertical resolution.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

