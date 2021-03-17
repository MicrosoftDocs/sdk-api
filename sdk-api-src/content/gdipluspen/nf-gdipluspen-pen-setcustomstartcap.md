---
UID: NF:gdipluspen.Pen.SetCustomStartCap
title: Pen::SetCustomStartCap (gdipluspen.h)
description: The Pen::SetCustomStartCap method sets the custom start cap for this Pen object.
helpviewer_keywords: ["Pen class [GDI+]","SetCustomStartCap method","Pen.SetCustomStartCap","Pen::SetCustomStartCap","SetCustomStartCap","SetCustomStartCap method [GDI+]","SetCustomStartCap method [GDI+]","Pen class","_gdiplus_CLASS_Pen_SetCustomStartCap_customCap_","gdiplus._gdiplus_CLASS_Pen_SetCustomStartCap_customCap_"]
old-location: gdiplus\_gdiplus_CLASS_Pen_SetCustomStartCap_customCap_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\setcustomstartcap.htm
ms.date: 12/05/2018
ms.keywords: Pen class [GDI+],SetCustomStartCap method, Pen.SetCustomStartCap, Pen::SetCustomStartCap, SetCustomStartCap, SetCustomStartCap method [GDI+], SetCustomStartCap method [GDI+],Pen class, _gdiplus_CLASS_Pen_SetCustomStartCap_customCap_, gdiplus._gdiplus_CLASS_Pen_SetCustomStartCap_customCap_
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
 - Pen::SetCustomStartCap
 - gdipluspen/Pen::SetCustomStartCap
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
 - Pen.SetCustomStartCap
---

# Pen::SetCustomStartCap


## -description

The <b>Pen::SetCustomStartCap</b> method sets the custom start cap for this 
			<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object.

## -parameters

### -param customCap [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-customlinecap">CustomLineCap</a>*</b>

Pointer to a 
					<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-customlinecap">CustomLineCap</a> object that specifies the custom start cap for this 
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



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-getcustomstartcap">Pen::GetCustomStartCap</a>



<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>