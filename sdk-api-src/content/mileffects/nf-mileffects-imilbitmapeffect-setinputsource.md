---
UID: NF:mileffects.IMILBitmapEffect.SetInputSource
title: IMILBitmapEffect::SetInputSource
author: windows-driver-content
description: Sets the effect input source.
old-location: wibe\_wibe_imilbitmapeffect_setinputsource.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffect\setinputsource.htm
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IMILBitmapEffect interface [WPF Bitmap Effects],SetInputSource method, IMILBitmapEffect.SetInputSource, IMILBitmapEffect::SetInputSource, SetInputSource, SetInputSource method [WPF Bitmap Effects], SetInputSource method [WPF Bitmap Effects],IMILBitmapEffect interface, _wibe_imilbitmapeffect_setinputsource, mileffects/IMILBitmapEffect::SetInputSource, wibe._wibe_imilbitmapeffect_setinputsource
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
-	Mileffects.h
api_name:
-	IMILBitmapEffect.SetInputSource
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



