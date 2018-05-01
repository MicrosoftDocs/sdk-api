---
UID: NF:mileffects.IMILBitmapEffectRenderContext.GetOutputDPI
title: IMILBitmapEffectRenderContext::GetOutputDPI method
author: windows-driver-content
description: Gets the output dots per inch (dpi).
old-location: wibe\_wibe_imilbitmapeffectrendercontext_getoutputdpi.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectrendercontext\getoutputdpi.htm
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: GetOutputDPI method [WPF Bitmap Effects], GetOutputDPI method [WPF Bitmap Effects], IMILBitmapEffectRenderContext interface, GetOutputDPI,IMILBitmapEffectRenderContext.GetOutputDPI, IMILBitmapEffectRenderContext, IMILBitmapEffectRenderContext interface [WPF Bitmap Effects], GetOutputDPI method, IMILBitmapEffectRenderContext::GetOutputDPI, _wibe_imilbitmapeffectrendercontext_getoutputdpi, mileffects/IMILBitmapEffectRenderContext::GetOutputDPI, wibe._wibe_imilbitmapeffectrendercontext_getoutputdpi
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MICUIELEMENTSTATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mileffects.dll
api_name:
-	IMILBitmapEffectRenderContext.GetOutputDPI
product: Windows
targetos: Windows
req.lib: 
req.dll: Mileffects.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMILBitmapEffectRenderContext::GetOutputDPI method


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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



