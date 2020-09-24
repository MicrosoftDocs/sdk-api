---
UID: NL:gdipluseffects.Tint
title: Tint (gdipluseffects.h)
description: The Tint class enables you to apply a tint to a bitmap.
helpviewer_keywords: ["Tint","Tint class [GDI+]","Tint class [GDI+]","described","_gdiplus_CLASS_Tint_Class","gdiplus._gdiplus_CLASS_Tint_Class","gdipluseffects/Tint"]
old-location: gdiplus\_gdiplus_CLASS_Tint_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\tint.htm
ms.date: 12/05/2018
ms.keywords: Tint, Tint class [GDI+], Tint class [GDI+],described, _gdiplus_CLASS_Tint_Class, gdiplus._gdiplus_CLASS_Tint_Class, gdipluseffects/Tint
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
 - Tint
 - gdipluseffects/Tint
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
 - Tint
---

# Tint class


## -description

The <b>Tint</b> class enables you to apply a tint to a bitmap. Pass the address of a <b>Tint</b> object to the <a href="/previous-versions/ms536058(v=vs.85)">Graphics::DrawImage</a> method or to the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-applyeffect(inbitmap_inint_ineffect_inrect_outrect_outbitmap)">Bitmap::ApplyEffect</a> method. To specify the nature of the tint, pass the address of a <a href="/windows/desktop/api/gdipluseffects/ns-gdipluseffects-tintparams">TintParams</a> structure to the <a href="/windows/desktop/api/gdipluseffects/nf-gdipluseffects-tint-setparameters">Tint::SetParameters</a> method of a <b>Tint</b> object.