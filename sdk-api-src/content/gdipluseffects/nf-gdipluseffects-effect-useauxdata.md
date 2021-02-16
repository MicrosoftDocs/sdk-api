---
UID: NF:gdipluseffects.Effect.UseAuxData
title: Effect::UseAuxData (gdipluseffects.h)
description: The Effect::UseAuxData method sets or clears a flag that specifies whether the Bitmap::ApplyEffect method should return a pointer to the auxiliary data that it creates.
helpviewer_keywords: ["Effect class [GDI+]","UseAuxData method","Effect.UseAuxData","Effect::UseAuxData","UseAuxData","UseAuxData method [GDI+]","UseAuxData method [GDI+]","Effect class","_gdiplus_CLASS_Effect_UseAuxData_","gdiplus._gdiplus_CLASS_Effect_UseAuxData_"]
old-location: gdiplus\_gdiplus_CLASS_Effect_UseAuxData_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\effectclass\effectmethods\useauxdata.htm
ms.date: 12/05/2018
ms.keywords: Effect class [GDI+],UseAuxData method, Effect.UseAuxData, Effect::UseAuxData, UseAuxData, UseAuxData method [GDI+], UseAuxData method [GDI+],Effect class, _gdiplus_CLASS_Effect_UseAuxData_, gdiplus._gdiplus_CLASS_Effect_UseAuxData_
req.header: gdipluseffects.h
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
ms.custom: 19H1
f1_keywords:
 - Effect::UseAuxData
 - gdipluseffects/Effect::UseAuxData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Effect.UseAuxData
---

# Effect::UseAuxData


## -description

The <b>Effect::UseAuxData</b> method sets or clears a flag that specifies whether the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-applyeffect(inbitmap_inint_ineffect_inrect_outrect_outbitmap)">Bitmap::ApplyEffect</a> method should return a pointer to the auxiliary data that it creates.

## -parameters

### -param useAuxDataFlag [in]

Type: <b>const BOOL</b>

Set to <b>TRUE</b> to specify that <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-applyeffect(inbitmap_inint_ineffect_inrect_outrect_outbitmap)">ApplyEffect</a> should return a pointer to its auxiliary data; <b>FALSE</b> otherwise.

## -see-also

<a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-effect">Effect</a>



<a href="/windows/desktop/api/gdipluseffects/nf-gdipluseffects-effect-getauxdata">Effect::GetAuxData</a>



<a href="/windows/desktop/api/gdipluseffects/nf-gdipluseffects-effect-getauxdatasize">Effect::GetAuxDataSize</a>