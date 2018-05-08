---
UID: NF:gdiplusheaders.CustomLineCap.SetWidthScale
title: CustomLineCap::SetWidthScale
author: windows-driver-content
description: The CustomLineCap::SetWidthScale method sets the value of the scale width. This is the amount to scale the custom line cap relative to the width of the Pen used to draw lines. The default value of 1.0 does not scale the line cap.
old-location: gdiplus\_gdiplus_CLASS_CustomLineCap_SetWidthScale_widthScale_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\customlinecapclass\customlinecapmethods\setwidthscale.htm
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: CustomLineCap class [GDI+],SetWidthScale method, CustomLineCap.SetWidthScale, CustomLineCap::SetWidthScale, SetWidthScale, SetWidthScale method [GDI+], SetWidthScale method [GDI+],CustomLineCap class, _gdiplus_CLASS_CustomLineCap_SetWidthScale_widthScale_, gdiplus._gdiplus_CLASS_CustomLineCap_SetWidthScale_widthScale_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.dll
api_name:
-	CustomLineCap.SetWidthScale
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# CustomLineCap::SetWidthScale


## -description


The <b>CustomLineCap::SetWidthScale</b> method sets the value of the scale width. This is the amount to scale the custom line cap relative to the width of the  <a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> used to draw lines. The default value of 1.0 does not scale the line cap.


## -parameters




### -param widthScale [in]

Type: <b>IN REAL</b>

Real number that specifies the scaling factor that will be used to scale the line width. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/bab33c8b-3203-4560-9e71-c112d528e20c">CustomLineCap</a>



<a href="https://msdn.microsoft.com/e72e402b-3cb7-4fc7-9050-ce00054da352">LineCap</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a>
 

 

