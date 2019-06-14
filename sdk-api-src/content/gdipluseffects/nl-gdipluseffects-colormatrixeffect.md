---
UID: NL:gdipluseffects.ColorMatrixEffect
title: ColorMatrixEffect (gdipluseffects.h)
author: windows-sdk-content
description: The ColorMatrixEffect class enables you to apply an affine transformation to a bitmap.
old-location: gdiplus\_gdiplus_CLASS_ColorMatrixEffect_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\colormatrixeffect.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ColorMatrixEffect, ColorMatrixEffect class [GDI+], ColorMatrixEffect class [GDI+],described, _gdiplus_CLASS_ColorMatrixEffect_Class, gdiplus._gdiplus_CLASS_ColorMatrixEffect_Class, gdipluseffects/ColorMatrixEffect
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
ms.custom: 19H1
---

# ColorMatrixEffect class


## -description


The <b>ColorMatrixEffect</b> class enables you to apply an affine transformation to a bitmap. Pass the address of a <b>ColorMatrixEffect</b> object to the <a href="https://docs.microsoft.com/previous-versions//ms536058(v=vs.85)">Graphics::DrawImage</a> method or to the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-applyeffect(inbitmap_inint_ineffect_inrect_outrect_outbitmap)">Bitmap::ApplyEffect</a> method. To specify the transformation, set the elements of a <a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix">ColorMatrix</a> structure, and pass the address of that structure to the <a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/nf-gdipluseffects-colormatrixeffect-setparameters">ColorMatrixEffect::SetParameters</a> method of a <b>ColorMatrixEffect</b> object.

