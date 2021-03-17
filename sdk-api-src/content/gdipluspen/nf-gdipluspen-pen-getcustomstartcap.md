---
UID: NF:gdipluspen.Pen.GetCustomStartCap
title: Pen::GetCustomStartCap (gdipluspen.h)
description: The Pen::GetCustomStartCap method gets the custom start cap currently set for this Pen object.
helpviewer_keywords: ["GetCustomStartCap","GetCustomStartCap method [GDI+]","GetCustomStartCap method [GDI+]","Pen class","Pen class [GDI+]","GetCustomStartCap method","Pen.GetCustomStartCap","Pen::GetCustomStartCap","_gdiplus_CLASS_Pen_GetCustomStartCap_customCap_","gdiplus._gdiplus_CLASS_Pen_GetCustomStartCap_customCap_"]
old-location: gdiplus\_gdiplus_CLASS_Pen_GetCustomStartCap_customCap_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\getcustomstartcap.htm
ms.date: 12/05/2018
ms.keywords: GetCustomStartCap, GetCustomStartCap method [GDI+], GetCustomStartCap method [GDI+],Pen class, Pen class [GDI+],GetCustomStartCap method, Pen.GetCustomStartCap, Pen::GetCustomStartCap, _gdiplus_CLASS_Pen_GetCustomStartCap_customCap_, gdiplus._gdiplus_CLASS_Pen_GetCustomStartCap_customCap_
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
 - Pen::GetCustomStartCap
 - gdipluspen/Pen::GetCustomStartCap
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
 - Pen.GetCustomStartCap
---

# Pen::GetCustomStartCap


## -description

The <b>Pen::GetCustomStartCap</b> method gets the custom start cap currently set for this 
			<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object.

## -parameters

### -param customCap [out]

Type: <b><a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-customlinecap">CustomLineCap</a>*</b>

Pointer to a 
					<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-customlinecap">CustomLineCap</a> object that receives the start cap of this 
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



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-getcustomendcap">Pen::GetCustomEndCap</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-setcustomendcap">Pen::SetCustomEndCap</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-setcustomstartcap">Pen::SetCustomStartCap</a>



<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>