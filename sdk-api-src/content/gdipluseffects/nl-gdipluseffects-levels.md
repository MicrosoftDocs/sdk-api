---
UID: NL:gdipluseffects.Levels
title: Levels (gdipluseffects.h)
description: The Levels class encompasses three bitmap adjustments:\_highlight, midtone, and shadow.
helpviewer_keywords: ["Levels","Levels class [GDI+]","Levels class [GDI+]","described","_gdiplus_CLASS_Levels_Class","gdiplus._gdiplus_CLASS_Levels_Class","gdipluseffects/Levels"]
old-location: gdiplus\_gdiplus_CLASS_Levels_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\levels.htm
ms.date: 12/05/2018
ms.keywords: Levels, Levels class [GDI+], Levels class [GDI+],described, _gdiplus_CLASS_Levels_Class, gdiplus._gdiplus_CLASS_Levels_Class, gdipluseffects/Levels
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
 - Levels
 - gdipluseffects/Levels
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
 - Levels
---

# Levels class


## -description

The <b>Levels</b> class encompasses three bitmap adjustments: highlight, midtone, and shadow. You can apply one or more of those adjustments to a bitmap by passing the address of a <b>Levels</b> object to the <a href="/previous-versions/ms536058(v=vs.85)">Graphics::DrawImage</a> method or to the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-applyeffect(inbitmap_inint_ineffect_inrect_outrect_outbitmap)">Bitmap::ApplyEffect</a> method. To specify the intensities of the adjustments, pass the address of a <a href="/windows/desktop/api/gdipluseffects/ns-gdipluseffects-levelsparams">LevelsParams</a> structure to the <a href="/windows/desktop/api/gdipluseffects/nf-gdipluseffects-levels-setparameters">Levels::SetParameters</a> method of a <b>Levels</b> object.