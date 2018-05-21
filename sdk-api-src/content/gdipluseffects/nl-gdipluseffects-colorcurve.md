---
UID: NL:gdipluseffects.ColorCurve
title: ColorCurve
author: windows-driver-content
description: The ColorCurve class encompasses eight separate adjustments:\_exposure, density, contrast, highlight, shadow, midtone, white saturation, and black saturation.
old-location: gdiplus\_gdiplus_CLASS_ColorCurve_Class.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\colorcurve.htm
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: ColorCurve, ColorCurve class [GDI+], ColorCurve class [GDI+],described, _gdiplus_CLASS_ColorCurve_Class, gdiplus._gdiplus_CLASS_ColorCurve_Class, gdipluseffects/ColorCurve
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: class
req.header: gdipluseffects.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
-	gdipluseffects.h
api_name:
-	ColorCurve
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ColorCurve class


## -description


The <b>ColorCurve</b> class encompasses eight separate adjustments: exposure, density, contrast, highlight, shadow, midtone, white saturation, and black saturation. You can apply one of those adjustments to a bitmap by passing the address of a <b>ColorCurve</b> object to the <a href="https://msdn.microsoft.com/cb85a7ac-5af0-45c7-8035-d7bc2827af6a">Graphics::DrawImage</a> method or to the <a href="https://msdn.microsoft.com/6b3d0a2f-acff-47a7-bc9f-6e9d659f683c">Bitmap::ApplyEffect</a> method. To specify the adjustment, the intensity of the adjustment, and the color channel to which the adjustment applies, pass the address of a <a href="https://msdn.microsoft.com/53204bea-b6b6-4a7c-a237-4754fbb92628">ColorCurveParams</a> structure to the <a href="https://msdn.microsoft.com/9e523edd-324d-473a-8a3b-36d99f4327ee">ColorCurve::SetParameters</a> method of a <b>ColorCurve</b> object.

