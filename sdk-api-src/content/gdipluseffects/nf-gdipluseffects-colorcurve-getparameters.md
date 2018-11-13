---
UID: NF:gdipluseffects.ColorCurve.GetParameters
title: ColorCurve::GetParameters
author: windows-sdk-content
description: The ColorCurve::GetParameters gets the current values of the parameters of this ColorCurve object.
old-location: gdiplus\_gdiplus_CLASS_ColorCurve_GetParameters_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\colorcurveclass\colorcurvemethods\getparameters.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ColorCurve class [GDI+],GetParameters method, ColorCurve.GetParameters, ColorCurve::GetParameters, GetParameters, GetParameters method [GDI+], GetParameters method [GDI+],ColorCurve class, _gdiplus_CLASS_ColorCurve_GetParameters_, gdiplus._gdiplus_CLASS_ColorCurve_GetParameters_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ColorCurve.GetParameters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
---

# ColorCurve::GetParameters


## -description


The <b>ColorCurve::GetParameters</b> gets the current values of the parameters of this <a href="https://msdn.microsoft.com/1ea62f08-f591-4da5-8fcc-74df7ddcebe4">ColorCurve</a> object.


## -parameters




### -param size [in]

Type: <b>UINT*</b>

Pointer to a <b>UINT</b> that specifies the size, in bytes, of a <a href="https://msdn.microsoft.com/53204bea-b6b6-4a7c-a237-4754fbb92628">ColorCurveParams</a> structure.


### -param parameters [out]

Type: <b><a href="https://msdn.microsoft.com/53204bea-b6b6-4a7c-a237-4754fbb92628">ColorCurveParams</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/53204bea-b6b6-4a7c-a237-4754fbb92628">ColorCurveParams</a> structure that receives the parameter values.


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/1ea62f08-f591-4da5-8fcc-74df7ddcebe4">ColorCurve</a>



<a href="https://msdn.microsoft.com/9e523edd-324d-473a-8a3b-36d99f4327ee">ColorCurve::SetParameters</a>
 

 

