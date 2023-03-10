---
UID: NF:gdipluspen.Pen.SetLineJoin
title: Pen::SetLineJoin (gdipluspen.h)
description: The Pen::SetLineJoin method sets the line join for this Pen object.
helpviewer_keywords: ["Pen class [GDI+]","SetLineJoin method","Pen.SetLineJoin","Pen::SetLineJoin","SetLineJoin","SetLineJoin method [GDI+]","SetLineJoin method [GDI+]","Pen class","_gdiplus_CLASS_Pen_SetLineJoin_lineJoin_","gdiplus._gdiplus_CLASS_Pen_SetLineJoin_lineJoin_"]
old-location: gdiplus\_gdiplus_CLASS_Pen_SetLineJoin_lineJoin_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\setlinejoin.htm
ms.date: 12/05/2018
ms.keywords: Pen class [GDI+],SetLineJoin method, Pen.SetLineJoin, Pen::SetLineJoin, SetLineJoin, SetLineJoin method [GDI+], SetLineJoin method [GDI+],Pen class, _gdiplus_CLASS_Pen_SetLineJoin_lineJoin_, gdiplus._gdiplus_CLASS_Pen_SetLineJoin_lineJoin_
req.header: gdipluspen.h
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
 - Pen::SetLineJoin
 - gdipluspen/Pen::SetLineJoin
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
 - Pen.SetLineJoin
---

# Pen::SetLineJoin


## -description

The <b>Pen::SetLineJoin</b> method sets the line join for this 
			<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object.

## -parameters

### -param lineJoin [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-linejoin">LineJoin</a></b>

Element of the 
					<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-linejoin">LineJoin</a> enumeration that specifies the join style used at the end of a line segment that meets another line segment.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-joining-lines-use">Joining Lines</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-linecap">LineCap</a>



<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-getendcap">Pen::GetEndCap</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-getstartcap">Pen::GetStartCap</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-setendcap">Pen::SetEndCap</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-setlinecap">Pen::SetLineCap</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-setstartcap">Pen::SetStartCap</a>



<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>