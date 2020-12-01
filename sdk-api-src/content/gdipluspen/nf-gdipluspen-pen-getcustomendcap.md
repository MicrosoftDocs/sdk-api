---
UID: NF:gdipluspen.Pen.GetCustomEndCap
title: Pen::GetCustomEndCap (gdipluspen.h)
description: The Pen::GetCustomEndCap method gets the custom end cap currently set for this Pen object.
helpviewer_keywords: ["GetCustomEndCap","GetCustomEndCap method [GDI+]","GetCustomEndCap method [GDI+]","Pen class","Pen class [GDI+]","GetCustomEndCap method","Pen.GetCustomEndCap","Pen::GetCustomEndCap","_gdiplus_CLASS_Pen_GetCustomEndCap_customCap_","gdiplus._gdiplus_CLASS_Pen_GetCustomEndCap_customCap_"]
old-location: gdiplus\_gdiplus_CLASS_Pen_GetCustomEndCap_customCap_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\getcustomendcap.htm
ms.date: 12/05/2018
ms.keywords: GetCustomEndCap, GetCustomEndCap method [GDI+], GetCustomEndCap method [GDI+],Pen class, Pen class [GDI+],GetCustomEndCap method, Pen.GetCustomEndCap, Pen::GetCustomEndCap, _gdiplus_CLASS_Pen_GetCustomEndCap_customCap_, gdiplus._gdiplus_CLASS_Pen_GetCustomEndCap_customCap_
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
 - Pen::GetCustomEndCap
 - gdipluspen/Pen::GetCustomEndCap
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
 - Pen.GetCustomEndCap
---

# Pen::GetCustomEndCap


## -description

The <b>Pen::GetCustomEndCap</b> method gets the custom end cap currently set for this 
			<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object.

## -parameters

### -param customCap [out]

Type: <b><a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-customlinecap">CustomLineCap</a>*</b>

Pointer to a 
					<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-customlinecap">CustomLineCap</a> object that receives the custom end cap of this 
					<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-drawing-a-custom-dashed-line-use">Drawing a Custom Dashed Line</a>



<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-getcustomstartcap">Pen::GetCustomStartCap</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-getendcap">Pen::GetEndCap</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-getstartcap">Pen::GetStartCap</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-setcustomendcap">Pen::SetCustomEndCap</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-setcustomstartcap">Pen::SetCustomStartCap</a>



<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>