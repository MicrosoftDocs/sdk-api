---
UID: NL:gdipluseffects.Blur
title: Blur (gdipluseffects.h)
author: windows-sdk-content
description: The Blur class enables you to apply a Gaussian blur effect to a bitmap and specify the nature of the blur.
old-location: gdiplus\_gdiplus_CLASS_Blur_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\blur.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Blur, Blur class [GDI+], Blur class [GDI+],described, _gdiplus_CLASS_Blur_Class, gdiplus._gdiplus_CLASS_Blur_Class, gdipluseffects/Blur
ms.topic: class
f1_keywords: 
 - "gdipluseffects/Blur"
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
 - Blur
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Blur class


## -description


The <b>Blur</b> class enables you to apply a Gaussian blur effect to a bitmap and specify the nature of the blur. Pass the address of a <b>Blur</b> object to the <a href="https://docs.microsoft.com/previous-versions/ms536058(v=vs.85)">Graphics::DrawImage</a> method or to the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-applyeffect(inbitmap_inint_ineffect_inrect_outrect_outbitmap)">Bitmap::ApplyEffect</a> method. To specify the nature of the blur, pass a <a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/ns-gdipluseffects-blurparams">BlurParams</a> structure to the <a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/nf-gdipluseffects-blur-setparameters">Blur::SetParameters</a> method of a <b>Blur</b> object.
		

