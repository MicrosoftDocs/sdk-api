---
UID: NF:gdipluspen.Pen.SetLineCap
title: Pen::SetLineCap (gdipluspen.h)
description: The Pen::SetLineCap method sets the cap styles for the start, end, and dashes in a line drawn with this pen.
helpviewer_keywords: ["Pen class [GDI+]","SetLineCap method","Pen.SetLineCap","Pen::SetLineCap","SetLineCap","SetLineCap method [GDI+]","SetLineCap method [GDI+]","Pen class","_gdiplus_CLASS_Pen_SetLineCap_startCap_endCap_dashCap_","gdiplus._gdiplus_CLASS_Pen_SetLineCap_startCap_endCap_dashCap_"]
old-location: gdiplus\_gdiplus_CLASS_Pen_SetLineCap_startCap_endCap_dashCap_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\setlinecap.htm
ms.date: 12/05/2018
ms.keywords: Pen class [GDI+],SetLineCap method, Pen.SetLineCap, Pen::SetLineCap, SetLineCap, SetLineCap method [GDI+], SetLineCap method [GDI+],Pen class, _gdiplus_CLASS_Pen_SetLineCap_startCap_endCap_dashCap_, gdiplus._gdiplus_CLASS_Pen_SetLineCap_startCap_endCap_dashCap_
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
 - Pen::SetLineCap
 - gdipluspen/Pen::SetLineCap
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
 - Pen.SetLineCap
---

# Pen::SetLineCap


## -description

The <b>Pen::SetLineCap</b> method sets the cap styles for the start, end, and dashes in a line drawn with this pen.

## -parameters

### -param startCap [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-linecap">LineCap</a></b>

Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-linecap">LineCap</a> enumeration that specifies the start cap of a line.

### -param endCap [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-linecap">LineCap</a></b>

Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-linecap">LineCap</a> enumeration that specifies the end cap of a line.

### -param dashCap [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-dashcap">DashCap</a></b>

Element of the 
					<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-dashcap">DashCap</a> enumeration that specifies the start and end caps of the dashes in a dashed line.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-drawing-a-line-with-line-caps-use">Drawing a Line with Line Caps</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-linecap">LineCap</a>



<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-getendcap">Pen::GetEndCap</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-getstartcap">Pen::GetStartCap</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-setcustomendcap">Pen::SetCustomEndCap</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-setcustomstartcap">Pen::SetCustomStartCap</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-setendcap">Pen::SetEndCap</a>



<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>