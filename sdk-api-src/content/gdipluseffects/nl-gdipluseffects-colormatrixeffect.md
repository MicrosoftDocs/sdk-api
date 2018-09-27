---
UID: NL:gdipluseffects.ColorMatrixEffect
title: ColorMatrixEffect
author: windows-sdk-content
description: The ColorMatrixEffect class enables you to apply an affine transformation to a bitmap.
old-location: gdiplus\_gdiplus_CLASS_ColorMatrixEffect_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\colormatrixeffect.htm
ms.author: windowssdkdev
ms.date: 09/12/2018
ms.keywords: ColorMatrixEffect, ColorMatrixEffect class [GDI+], ColorMatrixEffect class [GDI+],described, _gdiplus_CLASS_ColorMatrixEffect_Class, gdiplus._gdiplus_CLASS_ColorMatrixEffect_Class, gdipluseffects/ColorMatrixEffect
ms.prod: windows
ms.technology: windows-sdk
ms.topic: class
req.header: gdipluseffects.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - gdipluseffects.h
api_name:
 - ColorMatrixEffect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ColorMatrixEffect class


## -description


The <b>ColorMatrixEffect</b> class enables you to apply an affine transformation to a bitmap. Pass the address of a <b>ColorMatrixEffect</b> object to the <a href="https://msdn.microsoft.com/en-us/library/ms536058(v=VS.85).aspx">Graphics::DrawImage</a> method or to the <a href="https://msdn.microsoft.com/en-us/library/ms536284(v=VS.85).aspx">Bitmap::ApplyEffect</a> method. To specify the transformation, set the elements of a <a href="https://msdn.microsoft.com/en-us/library/ms534063(v=VS.85).aspx">ColorMatrix</a> structure, and pass the address of that structure to the <a href="https://msdn.microsoft.com/en-us/library/ms536233(v=VS.85).aspx">ColorMatrixEffect::SetParameters</a> method of a <b>ColorMatrixEffect</b> object.

