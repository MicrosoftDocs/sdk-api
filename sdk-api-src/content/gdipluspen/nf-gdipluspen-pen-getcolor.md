---
UID: NF:gdipluspen.Pen.GetColor
title: Pen::GetColor
author: windows-sdk-content
description: The Pen::GetColor method gets the color currently set for this Pen object.
old-location: gdiplus\_gdiplus_CLASS_Pen_GetColor_color_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\getcolor.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetColor, GetColor method [GDI+], GetColor method [GDI+],Pen class, Pen class [GDI+],GetColor method, Pen.GetColor, Pen::GetColor, _gdiplus_CLASS_Pen_GetColor_color_, gdiplus._gdiplus_CLASS_Pen_GetColor_color_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: WmfPlaceableFileHeader
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Pen.GetColor
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Pen::GetColor


## -description


The <b>Pen::GetColor</b> method gets the color currently set for this 
			<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object.


## -parameters




### -param color [out]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a> object that receives the color of this 
					<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a>



<a href="https://msdn.microsoft.com/cedef138-5047-4a72-8b89-5a95062a351c">Filling a Shape with a Solid Color</a>



<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>



<a href="https://msdn.microsoft.com/282393f0-e6f3-486f-a966-6137bac0d62b">Pen::SetColor</a>
 

 

