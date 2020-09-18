---
UID: NF:gdiplusheaders.CustomLineCap.SetStrokeJoin
title: CustomLineCap::SetStrokeJoin (gdiplusheaders.h)
description: The CustomLineCap::SetStrokeJoin method sets the style of line join for the stroke. The line join specifies how two lines that intersect within the GraphicsPath object that makes up the custom line cap are joined.
helpviewer_keywords: ["CustomLineCap class [GDI+]","SetStrokeJoin method","CustomLineCap.SetStrokeJoin","CustomLineCap::SetStrokeJoin","SetStrokeJoin","SetStrokeJoin method [GDI+]","SetStrokeJoin method [GDI+]","CustomLineCap class","_gdiplus_CLASS_CustomLineCap_SetStrokeJoin_lineJoin_","gdiplus._gdiplus_CLASS_CustomLineCap_SetStrokeJoin_lineJoin_"]
old-location: gdiplus\_gdiplus_CLASS_CustomLineCap_SetStrokeJoin_lineJoin_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\customlinecapclass\customlinecapmethods\setstrokejoin.htm
ms.date: 12/05/2018
ms.keywords: CustomLineCap class [GDI+],SetStrokeJoin method, CustomLineCap.SetStrokeJoin, CustomLineCap::SetStrokeJoin, SetStrokeJoin, SetStrokeJoin method [GDI+], SetStrokeJoin method [GDI+],CustomLineCap class, _gdiplus_CLASS_CustomLineCap_SetStrokeJoin_lineJoin_, gdiplus._gdiplus_CLASS_CustomLineCap_SetStrokeJoin_lineJoin_
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
 - CustomLineCap::SetStrokeJoin
 - gdiplusheaders/CustomLineCap::SetStrokeJoin
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
 - CustomLineCap.SetStrokeJoin
---

# CustomLineCap::SetStrokeJoin


## -description

The <b>CustomLineCap::SetStrokeJoin</b> method sets the style of line join for the stroke. The line join specifies how two lines that intersect within the <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object that makes up the custom line cap are joined.

## -parameters

### -param lineJoin [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-linejoin">LineJoin</a></b>

Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-linejoin">LineJoin</a> enumeration that specifies the line join that will be used for two lines that are drawn by the same pen and that have overlapping ends.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-customlinecap">CustomLineCap</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-linecap">LineCap</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-linejoin">LineJoin</a>



<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>