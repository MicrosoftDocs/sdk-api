---
UID: NS:gdipluseffects.ColorCurveParams
title: ColorCurveParams (gdipluseffects.h)
author: windows-sdk-content
description: A ColorCurveParams structure contains members that specify an adjustment to the colors of a bitmap.
old-location: gdiplus\_gdiplus_STRUC_ColorCurveParams.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\structures\colorcurveparams.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ColorCurveParams, ColorCurveParams structure [GDI+], _gdiplus_STRUC_ColorCurveParams, gdiplus._gdiplus_STRUC_ColorCurveParams, gdipluseffects/ColorCurveParams
ms.topic: struct
req.header: gdipluseffects.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - HeaderDef
api_location:
 - Gdipluseffects.h
api_name:
 - ColorCurveParams
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
---

# ColorCurveParams structure


## -description


A <b>ColorCurveParams</b> structure contains members that specify an adjustment to the colors of a bitmap.

The <a href="https://msdn.microsoft.com/en-us/library/ms534429(v=VS.85).aspx">ColorCurve</a> class encompasses eight separate adjustments: exposure, density, contrast, highlight, shadow, midtone, white saturation, and black saturation. You can apply one of those adjustments to a bitmap by following these steps.
<ol>
<li>Create and initialize a <b>ColorCurveParams</b> structure.</li>
<li>Pass the address of the <b>ColorCurveParams</b> structure to the <a href="https://msdn.microsoft.com/en-us/library/ms536241(v=VS.85).aspx">ColorCurve::SetParameters</a> method of a <a href="https://msdn.microsoft.com/en-us/library/ms534429(v=VS.85).aspx">ColorCurve</a> object.</li>
<li>Pass the address of the <a href="https://msdn.microsoft.com/en-us/library/ms534429(v=VS.85).aspx">ColorCurve</a> object to the <a href="https://msdn.microsoft.com/en-us/library/ms536058(v=VS.85).aspx">Graphics::DrawImage</a> method or to the <a href="https://msdn.microsoft.com/en-us/library/ms536284(v=VS.85).aspx">Bitmap::ApplyEffect</a> method.</li>
</ol>

## -struct-fields




### -field adjustment

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534098(v=VS.85).aspx">CurveAdjustments</a></b>

Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534098(v=VS.85).aspx">CurveAdjustments</a> enumeration that specifies the adjustment to be applied.


### -field channel

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534100(v=VS.85).aspx">CurveChannel</a></b>

Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534100(v=VS.85).aspx">CurveChannel</a> enumeration that specifies the color channel to which the adjustment applies.


### -field adjustValue

Type: <b>INT</b>

Integer that specifies the intensity of the adjustment. The range of acceptable values depends on which adjustment is being applied. To see the range of acceptable values for a particular adjustment, see the <a href="https://msdn.microsoft.com/en-us/library/ms534098(v=VS.85).aspx">CurveAdjustments</a> enumeration.

