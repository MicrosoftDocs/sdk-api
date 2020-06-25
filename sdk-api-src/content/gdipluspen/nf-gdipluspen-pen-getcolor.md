---
UID: NF:gdipluspen.Pen.GetColor
title: Pen::GetColor (gdipluspen.h)
description: The Pen::GetColor method gets the color currently set for this Pen object.
helpviewer_keywords: ["GetColor","GetColor method [GDI+]","GetColor method [GDI+]","Pen class","Pen class [GDI+]","GetColor method","Pen.GetColor","Pen::GetColor","_gdiplus_CLASS_Pen_GetColor_color_","gdiplus._gdiplus_CLASS_Pen_GetColor_color_"]
old-location: gdiplus\_gdiplus_CLASS_Pen_GetColor_color_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\getcolor.htm
ms.date: 12/05/2018
ms.keywords: GetColor, GetColor method [GDI+], GetColor method [GDI+],Pen class, Pen class [GDI+],GetColor method, Pen.GetColor, Pen::GetColor, _gdiplus_CLASS_Pen_GetColor_color_, gdiplus._gdiplus_CLASS_Pen_GetColor_color_
f1_keywords:
- gdipluspen/Pen.GetColor
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Gdiplus.dll
api_name:
- Pen.GetColor
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Pen::GetColor


## -description


The <b>Pen::GetColor</b> method gets the color currently set for this 
			<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object.


## -parameters




### -param color [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>*</b>

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a> object that receives the color of this 
					<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object. 


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-filling-a-shape-with-a-solid-color-use">Filling a Shape with a Solid Color</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-setcolor">Pen::SetColor</a>
 

 

