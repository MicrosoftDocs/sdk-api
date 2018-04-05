---
UID: NF:mileffects.IMILBitmapEffect.GetParentEffect
title: IMILBitmapEffect::GetParentEffect method
author: windows-driver-content
description: Gets a parent of the effect.
old-location: wibe\_wibe_imilbitmapeffect_getparenteffect.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffect\getparenteffect.htm
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: GetParentEffect method [WPF Bitmap Effects], GetParentEffect method [WPF Bitmap Effects], IMILBitmapEffect interface, GetParentEffect,IMILBitmapEffect.GetParentEffect, IMILBitmapEffect, IMILBitmapEffect interface [WPF Bitmap Effects], GetParentEffect method, IMILBitmapEffect::GetParentEffect, _wibe_imilbitmapeffect_getparenteffect, mileffects/IMILBitmapEffect::GetParentEffect, wibe._wibe_imilbitmapeffect_getparenteffect
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
-	IMILBitmapEffect.GetParentEffect
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMILBitmapEffect::GetParentEffect method


## -description


Gets a parent of the effect.


## -parameters




### -param ppParentEffect [out, retval]

Type: <b><a href="https://msdn.microsoft.com/a8ca1b39-f1b9-40b5-bcec-bf2e3182b9aa">IMILBitmapEffectGroup</a>**</b>

A pointer that receives a pointer to the <a href="https://msdn.microsoft.com/a8ca1b39-f1b9-40b5-bcec-bf2e3182b9aa">IMILBitmapEffectGroup</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



