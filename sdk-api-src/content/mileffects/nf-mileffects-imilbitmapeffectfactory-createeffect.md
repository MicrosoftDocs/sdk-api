---
UID: NF:mileffects.IMILBitmapEffectFactory.CreateEffect
title: IMILBitmapEffectFactory::CreateEffect (mileffects.h)
description: Creates an IMILBitmapEffect object.
helpviewer_keywords: ["CreateEffect","CreateEffect method [WPF Bitmap Effects]","CreateEffect method [WPF Bitmap Effects]","IMILBitmapEffectFactory interface","IMILBitmapEffectFactory interface [WPF Bitmap Effects]","CreateEffect method","IMILBitmapEffectFactory.CreateEffect","IMILBitmapEffectFactory::CreateEffect","_wibe_imilbitmapeffectfactory_createeffect","mileffects/IMILBitmapEffectFactory::CreateEffect","wibe._wibe_imilbitmapeffectfactory_createeffect"]
old-location: wibe\_wibe_imilbitmapeffectfactory_createeffect.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectfactory\createeffect.htm
ms.date: 12/05/2018
ms.keywords: CreateEffect, CreateEffect method [WPF Bitmap Effects], CreateEffect method [WPF Bitmap Effects],IMILBitmapEffectFactory interface, IMILBitmapEffectFactory interface [WPF Bitmap Effects],CreateEffect method, IMILBitmapEffectFactory.CreateEffect, IMILBitmapEffectFactory::CreateEffect, _wibe_imilbitmapeffectfactory_createeffect, mileffects/IMILBitmapEffectFactory::CreateEffect, wibe._wibe_imilbitmapeffectfactory_createeffect
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
 - IMILBitmapEffectFactory::CreateEffect
 - mileffects/IMILBitmapEffectFactory::CreateEffect
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
 - IMILBitmapEffectFactory.CreateEffect
---

# IMILBitmapEffectFactory::CreateEffect


## -description

Creates an <a href="/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffect">IMILBitmapEffect</a> object.

## -parameters

### -param pguidEffect [in]

Type: <b>const GUID*</b>

A pointer to the GUID of the effect to create.

### -param ppEffect [out]

Type: <b><a href="/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffect">IMILBitmapEffect</a>**</b>

A pointer that receives a pointer to a new <a href="/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectprimitive">IMILBitmapEffectPrimitive</a> object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.