---
UID: NF:mileffects.IMILBitmapEffect.GetOutput
title: IMILBitmapEffect::GetOutput (mileffects.h)
description: Gets the output of the effect.
helpviewer_keywords: ["GetOutput","GetOutput method [WPF Bitmap Effects]","GetOutput method [WPF Bitmap Effects]","IMILBitmapEffect interface","IMILBitmapEffect interface [WPF Bitmap Effects]","GetOutput method","IMILBitmapEffect.GetOutput","IMILBitmapEffect::GetOutput","_wibe_imilbitmapeffect_getoutput","mileffects/IMILBitmapEffect::GetOutput","wibe._wibe_imilbitmapeffect_getoutput"]
old-location: wibe\_wibe_imilbitmapeffect_getoutput.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffect\getoutput.htm
ms.date: 12/05/2018
ms.keywords: GetOutput, GetOutput method [WPF Bitmap Effects], GetOutput method [WPF Bitmap Effects],IMILBitmapEffect interface, IMILBitmapEffect interface [WPF Bitmap Effects],GetOutput method, IMILBitmapEffect.GetOutput, IMILBitmapEffect::GetOutput, _wibe_imilbitmapeffect_getoutput, mileffects/IMILBitmapEffect::GetOutput, wibe._wibe_imilbitmapeffect_getoutput
f1_keywords:
- mileffects/IMILBitmapEffect.GetOutput
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Mileffects.h
api_name:
- IMILBitmapEffect.GetOutput
targetos: Windows
req.typenames: 
req.redist: Microsoft .Net 3.0
ms.custom: 19H1
---

# IMILBitmapEffect::GetOutput


## -description


Gets the output of the effect.


## -parameters




### -param uiIndex [in]

Type: <b>ULONG</b>

The output index.


### -param pContext [in]

Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectrendercontext">IMILBitmapEffectRenderContext</a>*</b>

A pointer to the render context of the effect.


### -param ppBitmapSource [out, retval]

Type: <b>IWICBitmapSource**</b>

A pointer that receives a pointer to the effect's output.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



