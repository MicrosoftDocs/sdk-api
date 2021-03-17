---
UID: NF:gdiplusheaders.CustomLineCap.SetWidthScale
title: CustomLineCap::SetWidthScale (gdiplusheaders.h)
description: The CustomLineCap::SetWidthScale method sets the value of the scale width. This is the amount to scale the custom line cap relative to the width of the Pen used to draw lines. The default value of 1.0 does not scale the line cap.
helpviewer_keywords: ["CustomLineCap class [GDI+]","SetWidthScale method","CustomLineCap.SetWidthScale","CustomLineCap::SetWidthScale","SetWidthScale","SetWidthScale method [GDI+]","SetWidthScale method [GDI+]","CustomLineCap class","_gdiplus_CLASS_CustomLineCap_SetWidthScale_widthScale_","gdiplus._gdiplus_CLASS_CustomLineCap_SetWidthScale_widthScale_"]
old-location: gdiplus\_gdiplus_CLASS_CustomLineCap_SetWidthScale_widthScale_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\customlinecapclass\customlinecapmethods\setwidthscale.htm
ms.date: 12/05/2018
ms.keywords: CustomLineCap class [GDI+],SetWidthScale method, CustomLineCap.SetWidthScale, CustomLineCap::SetWidthScale, SetWidthScale, SetWidthScale method [GDI+], SetWidthScale method [GDI+],CustomLineCap class, _gdiplus_CLASS_CustomLineCap_SetWidthScale_widthScale_, gdiplus._gdiplus_CLASS_CustomLineCap_SetWidthScale_widthScale_
req.header: gdiplusheaders.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - CustomLineCap::SetWidthScale
 - gdiplusheaders/CustomLineCap::SetWidthScale
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
 - CustomLineCap.SetWidthScale
---

# CustomLineCap::SetWidthScale


## -description

The <b>CustomLineCap::SetWidthScale</b> method sets the value of the scale width. This is the amount to scale the custom line cap relative to the width of the  <a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> used to draw lines. The default value of 1.0 does not scale the line cap.

## -parameters

### -param widthScale [in]

Type: <b>IN REAL</b>

Real number that specifies the scaling factor that will be used to scale the line width.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-customlinecap">CustomLineCap</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-linecap">LineCap</a>



<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>