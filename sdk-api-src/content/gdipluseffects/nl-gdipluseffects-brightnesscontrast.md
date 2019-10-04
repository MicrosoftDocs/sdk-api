---
UID: NL:gdipluseffects.BrightnessContrast
title: BrightnessContrast (gdipluseffects.h)
author: windows-sdk-content
description: The BrightnessContrast class enables you to change the brightness and contrast of a bitmap.
old-location: gdiplus\_gdiplus_CLASS_BrightnessContrast_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\brightnesscontrast.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: BrightnessContrast, BrightnessContrast class [GDI+], BrightnessContrast class [GDI+],described, _gdiplus_CLASS_BrightnessContrast_Class, gdiplus._gdiplus_CLASS_BrightnessContrast_Class, gdipluseffects/BrightnessContrast
ms.topic: class
f1_keywords: 
 - "gdipluseffects/BrightnessContrast"
dev_langs:
 - c++
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
 - BrightnessContrast
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# BrightnessContrast class


## -description


The <b>BrightnessContrast</b> class enables you to change the brightness and contrast of a bitmap. Pass the address of a <b>BrightnessContrast</b> object to the <a href="https://docs.microsoft.com/previous-versions/ms536058(v=vs.85)">Graphics::DrawImage</a> method or to the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-applyeffect(inbitmap_inint_ineffect_inrect_outrect_outbitmap)">Bitmap::ApplyEffect</a> method. To specify the brightness and contrast levels, pass a <a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/ns-gdipluseffects-brightnesscontrastparams">BrightnessContrastParams</a> structure to the <a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/nf-gdipluseffects-brightnesscontrast-setparameters">BrightnessContrast::SetParameters</a> method of a <b>BrightnessContrast</b> object.

