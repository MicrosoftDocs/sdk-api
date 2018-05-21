---
UID: NF:gdipluseffects.ColorCurve.SetParameters
title: ColorCurve::SetParameters
author: windows-driver-content
description: The ColorCurve::SetParameters method sets the parameters of this ColorCurve object.
old-location: gdiplus\_gdiplus_CLASS_ColorCurve_SetParameters_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\colorcurveclass\colorcurvemethods\setparameters.htm
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: ColorCurve class [GDI+],SetParameters method, ColorCurve.SetParameters, ColorCurve::SetParameters, SetParameters, SetParameters method [GDI+], SetParameters method [GDI+],ColorCurve class, _gdiplus_CLASS_ColorCurve_SetParameters_, gdiplus._gdiplus_CLASS_ColorCurve_SetParameters_
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.dll
api_name:
-	ColorCurve.SetParameters
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ColorCurve::SetParameters


## -description


The <b>ColorCurve::SetParameters</b> method sets the parameters of this <a href="https://msdn.microsoft.com/1ea62f08-f591-4da5-8fcc-74df7ddcebe4">ColorCurve</a> object.


## -parameters




### -param parameters [in]

Type: <b>const <a href="https://msdn.microsoft.com/53204bea-b6b6-4a7c-a237-4754fbb92628">ColorCurveParams</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/53204bea-b6b6-4a7c-a237-4754fbb92628">ColorCurveParams</a> structure that specifies the parameters.


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/1ea62f08-f591-4da5-8fcc-74df7ddcebe4">ColorCurve</a>



<a href="https://msdn.microsoft.com/796cba21-9606-47af-9db0-909ca1c2e0ff">ColorCurve::GetParameters</a>
 

 

