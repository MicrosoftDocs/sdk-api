---
UID: NL:gdipluseffects.Sharpen
title: Sharpen (gdipluseffects.h)
description: The Sharpen class enables you to adjust the sharpness of a bitmap.
helpviewer_keywords: ["Sharpen","Sharpen class [GDI+]","Sharpen class [GDI+]","described","_gdiplus_CLASS_Sharpen_Class","gdiplus._gdiplus_CLASS_Sharpen_Class","gdipluseffects/Sharpen"]
old-location: gdiplus\_gdiplus_CLASS_Sharpen_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\sharpen.htm
ms.date: 12/05/2018
ms.keywords: Sharpen, Sharpen class [GDI+], Sharpen class [GDI+],described, _gdiplus_CLASS_Sharpen_Class, gdiplus._gdiplus_CLASS_Sharpen_Class, gdipluseffects/Sharpen
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Sharpen
 - gdipluseffects/Sharpen
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gdipluseffects.h
api_name:
 - Sharpen
---

# Sharpen class


## -description

The <b>Sharpen</b> class enables you to adjust the sharpness of a bitmap. Pass the address of a <b>Sharpen</b> object to the <a href="/previous-versions/ms536058(v=vs.85)">Graphics::DrawImage</a> method or to the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-applyeffect(inbitmap_inint_ineffect_inrect_outrect_outbitmap)">Bitmap::ApplyEffect</a> method. To specify the nature of the sharpening adjustment, pass the address of a <a href="/windows/desktop/api/gdipluseffects/ns-gdipluseffects-sharpenparams">SharpenParams</a> structure to the <a href="/windows/desktop/api/gdipluseffects/nf-gdipluseffects-sharpen-setparameters">Sharpen::SetParameters</a> method of a <b>Sharpen</b> object.