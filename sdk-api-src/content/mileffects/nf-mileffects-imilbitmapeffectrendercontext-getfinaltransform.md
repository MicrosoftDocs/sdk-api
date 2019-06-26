---
UID: NF:mileffects.IMILBitmapEffectRenderContext.GetFinalTransform
title: IMILBitmapEffectRenderContext::GetFinalTransform (mileffects.h)
author: windows-sdk-content
description: Gets the final MILMatrixF transform.
old-location: wibe\_wibe_imilbitmapeffectrendercontext_getfinaltransform.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectrendercontext\getfinaltransform.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetFinalTransform, GetFinalTransform method [WPF Bitmap Effects], GetFinalTransform method [WPF Bitmap Effects],IMILBitmapEffectRenderContext interface, IMILBitmapEffectRenderContext interface [WPF Bitmap Effects],GetFinalTransform method, IMILBitmapEffectRenderContext.GetFinalTransform, IMILBitmapEffectRenderContext::GetFinalTransform, _wibe_imilbitmapeffectrendercontext_getfinaltransform, mileffects/IMILBitmapEffectRenderContext::GetFinalTransform, wibe._wibe_imilbitmapeffectrendercontext_getfinaltransform
ms.topic: method
f1_keywords: 
 - "mileffects/IMILBitmapEffectRenderContext.GetFinalTransform"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mileffects.dll
api_name:
 - IMILBitmapEffectRenderContext.GetFinalTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: Microsoft .Net 3.0
ms.custom: 19H1
---

# IMILBitmapEffectRenderContext::GetFinalTransform


## -description


Gets the final <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/ns-mileffects-milmatrixf">MILMatrixF</a> transform.


## -parameters




### -param pMatrix [out]

Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/ns-mileffects-milmatrixf">MILMatrixF</a>*</b>

The final transform.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



