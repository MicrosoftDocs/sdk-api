---
UID: NF:mileffects.IMILBitmapEffect.GetParentEffect
title: IMILBitmapEffect::GetParentEffect (mileffects.h)
description: Gets a parent of the effect.
helpviewer_keywords: ["GetParentEffect","GetParentEffect method [WPF Bitmap Effects]","GetParentEffect method [WPF Bitmap Effects]","IMILBitmapEffect interface","IMILBitmapEffect interface [WPF Bitmap Effects]","GetParentEffect method","IMILBitmapEffect.GetParentEffect","IMILBitmapEffect::GetParentEffect","_wibe_imilbitmapeffect_getparenteffect","mileffects/IMILBitmapEffect::GetParentEffect","wibe._wibe_imilbitmapeffect_getparenteffect"]
old-location: wibe\_wibe_imilbitmapeffect_getparenteffect.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffect\getparenteffect.htm
ms.date: 12/05/2018
ms.keywords: GetParentEffect, GetParentEffect method [WPF Bitmap Effects], GetParentEffect method [WPF Bitmap Effects],IMILBitmapEffect interface, IMILBitmapEffect interface [WPF Bitmap Effects],GetParentEffect method, IMILBitmapEffect.GetParentEffect, IMILBitmapEffect::GetParentEffect, _wibe_imilbitmapeffect_getparenteffect, mileffects/IMILBitmapEffect::GetParentEffect, wibe._wibe_imilbitmapeffect_getparenteffect
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
 - IMILBitmapEffect::GetParentEffect
 - mileffects/IMILBitmapEffect::GetParentEffect
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
 - IMILBitmapEffect.GetParentEffect
---

# IMILBitmapEffect::GetParentEffect


## -description

Gets a parent of the effect.

## -parameters

### -param ppParentEffect [out, retval]

Type: <b><a href="/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectgroup">IMILBitmapEffectGroup</a>**</b>

A pointer that receives a pointer to the <a href="/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectgroup">IMILBitmapEffectGroup</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.