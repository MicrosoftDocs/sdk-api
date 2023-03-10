---
UID: NL:gdipluseffects.RedEyeCorrection
title: RedEyeCorrection (gdipluseffects.h)
description: The RedEyeCorrection class enables you to correct the red eyes that sometimes occur in flash photographs.
helpviewer_keywords: ["RedEyeCorrection","RedEyeCorrection class [GDI+]","RedEyeCorrection class [GDI+]","described","_gdiplus_CLASS_RedEyeCorrection_Class","gdiplus._gdiplus_CLASS_RedEyeCorrection_Class","gdipluseffects/RedEyeCorrection"]
old-location: gdiplus\_gdiplus_CLASS_RedEyeCorrection_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\redeyecorrection.htm
ms.date: 12/05/2018
ms.keywords: RedEyeCorrection, RedEyeCorrection class [GDI+], RedEyeCorrection class [GDI+],described, _gdiplus_CLASS_RedEyeCorrection_Class, gdiplus._gdiplus_CLASS_RedEyeCorrection_Class, gdipluseffects/RedEyeCorrection
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
 - RedEyeCorrection
 - gdipluseffects/RedEyeCorrection
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
 - RedEyeCorrection
---

# RedEyeCorrection class


## -description

The <b>RedEyeCorrection</b> class enables you to correct the red eyes that sometimes occur in flash photographs. Pass the address of a <b>RedEyeCorrection</b> object to the <a href="/previous-versions/ms536058(v=vs.85)">Graphics::DrawImage</a> method or to the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-applyeffect(inbitmap_inint_ineffect_inrect_outrect_outbitmap)">Bitmap::ApplyEffect</a> method. To specify areas of the bitmap that have red eyes, pass a <a href="/windows/desktop/api/gdipluseffects/ns-gdipluseffects-redeyecorrectionparams">RedEyeCorrectionParams</a> structure to the <a href="/windows/desktop/api/gdipluseffects/nf-gdipluseffects-redeyecorrection-setparameters">RedEyeCorrection::SetParameters</a> method of a <b>RedEyeCorrection</b> object.