---
UID: NF:gdiplusheaders.Bitmap.ApplyEffect(Effect,RECT)
title: Bitmap::ApplyEffect(Effect,RECT)
author: windows-sdk-content
description: The Bitmap::ApplyEffect method alters this Bitmap object by applying a specified effect.
old-location: gdiplus\_gdiplus_CLASS_Bitmap_ApplyEffect_Effect_effect_RECT_ROI_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapapplyeffectmethods\applyeffect_effecteffect_rectroi.htm
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: ApplyEffect, ApplyEffect method [GDI+], ApplyEffect method [GDI+],Bitmap class, Bitmap class [GDI+],ApplyEffect method, Bitmap.ApplyEffect, Bitmap.ApplyEffect(Effect*,RECT*), Bitmap.ApplyEffect(Effect,RECT), Bitmap::ApplyEffect, Bitmap::ApplyEffect(Effect,RECT), _gdiplus_CLASS_Bitmap_ApplyEffect_Effect_effect_RECT_ROI_, gdiplus._gdiplus_CLASS_Bitmap_ApplyEffect_Effect_effect_RECT_ROI_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusheaders.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Bitmap.ApplyEffect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
---

# Bitmap::ApplyEffect(Effect,RECT)


## -description


The <b>Bitmap::ApplyEffect</b> method alters this <a href="https://msdn.microsoft.com/f9826772-bb8a-4339-9cea-f77637f971b2">Bitmap</a> object by applying a specified effect.


## -parameters




### -param effect [in]

Type: <b><a href="https://msdn.microsoft.com/7b32aad2-ba44-46a6-8315-d55fed2d9391">Effect</a>*</b>

Pointer to an instance of a descendant of the <a href="https://msdn.microsoft.com/7b32aad2-ba44-46a6-8315-d55fed2d9391">Effect</a> class. The descendant (for example, a <a href="https://msdn.microsoft.com/a061b15b-bce4-4b38-adba-836b6b295c80">Blur</a> object) specifies the effect that is applied.


### -param ROI [in]

Type: <b>RECT*</b>

Pointer to a RECT structure that specifies the portion of the input bitmap to which the effect is applied. Pass <b>NULL</b> to specify that the effect applies to the entire input bitmap.


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/f9826772-bb8a-4339-9cea-f77637f971b2">Bitmap</a>



<a href="https://msdn.microsoft.com/6b3d0a2f-acff-47a7-bc9f-6e9d659f683c">Bitmap::ApplyEffect Methods</a>
 

 

