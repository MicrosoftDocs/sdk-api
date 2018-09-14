---
UID: NL:gdipluseffects.ColorCurve
title: ColorCurve
author: windows-sdk-content
description: The ColorCurve class encompasses eight separate adjustments:\_exposure, density, contrast, highlight, shadow, midtone, white saturation, and black saturation.
old-location: gdiplus\_gdiplus_CLASS_ColorCurve_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\colorcurve.htm
ms.author: windowssdkdev
ms.date: 09/12/2018
ms.keywords: ColorCurve, ColorCurve class [GDI+], ColorCurve class [GDI+],described, _gdiplus_CLASS_ColorCurve_Class, gdiplus._gdiplus_CLASS_ColorCurve_Class, gdipluseffects/ColorCurve
ms.prod: windows
ms.technology: windows-sdk
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gdipluseffects.h
api_name:
 - ColorCurve
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ColorCurve class


## -description


The <b>ColorCurve</b> class encompasses eight separate adjustments: exposure, density, contrast, highlight, shadow, midtone, white saturation, and black saturation. You can apply one of those adjustments to a bitmap by passing the address of a <b>ColorCurve</b> object to the <a href="https://msdn.microsoft.com/en-us/library/ms536058(v=VS.85).aspx">Graphics::DrawImage</a> method or to the <a href="https://msdn.microsoft.com/en-us/library/ms536284(v=VS.85).aspx">Bitmap::ApplyEffect</a> method. To specify the adjustment, the intensity of the adjustment, and the color channel to which the adjustment applies, pass the address of a <a href="https://msdn.microsoft.com/en-us/library/ms534060(v=VS.85).aspx">ColorCurveParams</a> structure to the <a href="https://msdn.microsoft.com/en-us/library/ms536241(v=VS.85).aspx">ColorCurve::SetParameters</a> method of a <b>ColorCurve</b> object.

