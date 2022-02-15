---
UID: NF:mileffects.IMILBitmapEffect.SetInputSource
title: IMILBitmapEffect::SetInputSource (mileffects.h)
description: Sets the effect input source.
helpviewer_keywords: ["IMILBitmapEffect interface [WPF Bitmap Effects]","SetInputSource method","IMILBitmapEffect.SetInputSource","IMILBitmapEffect::SetInputSource","SetInputSource","SetInputSource method [WPF Bitmap Effects]","SetInputSource method [WPF Bitmap Effects]","IMILBitmapEffect interface","_wibe_imilbitmapeffect_setinputsource","mileffects/IMILBitmapEffect::SetInputSource","wibe._wibe_imilbitmapeffect_setinputsource"]
old-location: wibe\_wibe_imilbitmapeffect_setinputsource.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffect\setinputsource.htm
ms.date: 12/05/2018
ms.keywords: IMILBitmapEffect interface [WPF Bitmap Effects],SetInputSource method, IMILBitmapEffect.SetInputSource, IMILBitmapEffect::SetInputSource, SetInputSource, SetInputSource method [WPF Bitmap Effects], SetInputSource method [WPF Bitmap Effects],IMILBitmapEffect interface, _wibe_imilbitmapeffect_setinputsource, mileffects/IMILBitmapEffect::SetInputSource, wibe._wibe_imilbitmapeffect_setinputsource
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
 - IMILBitmapEffect::SetInputSource
 - mileffects/IMILBitmapEffect::SetInputSource
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
 - IMILBitmapEffect.SetInputSource
---

# IMILBitmapEffect::SetInputSource


## -description

Sets the effect input source.

## -parameters

### -param uiIndex [in]

Type: <b>ULONG</b>

The input index.

### -param pBitmapSource [in]

Type: <b>IWICBitmapSource*</b>

A pointer to the effect's bitmap source.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

