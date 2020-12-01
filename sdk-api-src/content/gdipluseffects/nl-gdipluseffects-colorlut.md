---
UID: NL:gdipluseffects.ColorLUT
title: ColorLUT (gdipluseffects.h)
description: A ColorLUTParams structure has four members, each being a lookup table for a particular color channel:\_alpha, red, green, or blue.
helpviewer_keywords: ["ColorLUT","ColorLUT class [GDI+]","ColorLUT class [GDI+]","described","_gdiplus_CLASS_ColorLUT_Class","gdiplus._gdiplus_CLASS_ColorLUT_Class","gdipluseffects/ColorLUT"]
old-location: gdiplus\_gdiplus_CLASS_ColorLUT_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\colorlut.htm
ms.date: 12/05/2018
ms.keywords: ColorLUT, ColorLUT class [GDI+], ColorLUT class [GDI+],described, _gdiplus_CLASS_ColorLUT_Class, gdiplus._gdiplus_CLASS_ColorLUT_Class, gdipluseffects/ColorLUT
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
 - ColorLUT
 - gdipluseffects/ColorLUT
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
 - ColorLUT
---

# ColorLUT class


## -description

A <a href="/windows/desktop/api/gdipluseffects/ns-gdipluseffects-colorlutparams">ColorLUTParams</a> structure has four members, each being a lookup table for a particular color channel: alpha, red, green, or blue. The lookup tables can be used to make custom color adjustments to bitmaps. Each lookup table is an array of 256 bytes that you can set to values of your choice. After you have initialized a <b>ColorLUTParams</b> structure, pass its address to the <a href="/windows/desktop/api/gdipluseffects/nf-gdipluseffects-colorlut-setparameters">ColorLUT::SetParameters</a> method of a <b>ColorLUT</b> object. Then pass the address of that <b>ColorLUT</b> object to the <a href="/previous-versions/ms536058(v=vs.85)">Graphics::DrawImage</a> method or to the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-applyeffect(inbitmap_inint_ineffect_inrect_outrect_outbitmap)">Bitmap::ApplyEffect</a> method.