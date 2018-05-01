---
UID: NF:mileffects.IMILBitmapEffectRenderContext.SetUseSoftwareRenderer
title: IMILBitmapEffectRenderContext::SetUseSoftwareRenderer method
author: windows-driver-content
description: Sets a value to indicate whether to use software rendering.
old-location: wibe\_wibe_imilbitmapeffectrendercontext_setusesoftwarerenderer.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectrendercontext\setusesoftwarerenderer.htm
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: IMILBitmapEffectRenderContext, IMILBitmapEffectRenderContext interface [WPF Bitmap Effects], SetUseSoftwareRenderer method, IMILBitmapEffectRenderContext::SetUseSoftwareRenderer, SetUseSoftwareRenderer method [WPF Bitmap Effects], SetUseSoftwareRenderer method [WPF Bitmap Effects], IMILBitmapEffectRenderContext interface, SetUseSoftwareRenderer,IMILBitmapEffectRenderContext.SetUseSoftwareRenderer, _wibe_imilbitmapeffectrendercontext_setusesoftwarerenderer, mileffects/IMILBitmapEffectRenderContext::SetUseSoftwareRenderer, wibe._wibe_imilbitmapeffectrendercontext_setusesoftwarerenderer
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
-	IMILBitmapEffectRenderContext.SetUseSoftwareRenderer
product: Windows
targetos: Windows
req.lib: 
req.dll: Mileffects.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMILBitmapEffectRenderContext::SetUseSoftwareRenderer method


## -description


Sets a value to indicate whether to use software rendering.


## -parameters




### -param fSoftware [in]

Type: <b>VARIANT_BOOL</b>

A value indicating whether to use software rendering.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



All Windows Presentation Foundation (WPF) effects are software rendered at this time.



