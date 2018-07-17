---
UID: NF:gdipluseffects.ColorMatrixEffect.SetParameters
title: ColorMatrixEffect::SetParameters
author: windows-sdk-content
description: The ColorMatrixEffect::SetParameters method sets the 5x5 color matrix of this ColorMatrixEffect object.
old-location: gdiplus\_gdiplus_CLASS_ColorMatrixEffect_SetParameters_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\colormatrixeffectclass\colormatrixeffectmethods\setparameters.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: ColorMatrixEffect class [GDI+],SetParameters method, ColorMatrixEffect.SetParameters, ColorMatrixEffect::SetParameters, SetParameters, SetParameters method [GDI+], SetParameters method [GDI+],ColorMatrixEffect class, _gdiplus_CLASS_ColorMatrixEffect_SetParameters_, gdiplus._gdiplus_CLASS_ColorMatrixEffect_SetParameters_
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - ColorMatrixEffect.SetParameters
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ColorMatrixEffect::SetParameters


## -description


The <b>ColorMatrixEffect::SetParameters</b> method sets the 5x5 color matrix of this <a href="https://msdn.microsoft.com/library/ms534431(v=VS.85).aspx">ColorMatrixEffect</a> object.


## -parameters




### -param matrix [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/ms534063(v=VS.85).aspx">ColorMatrix</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/library/ms534063(v=VS.85).aspx">ColorMatrix</a> object that specifies the 5x5 color matrix. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/library/ms534431(v=VS.85).aspx">ColorMatrixEffect</a>



<a href="https://msdn.microsoft.com/library/ms536232(v=VS.85).aspx">ColorMatrixEffect::GetParameters</a>



<a href="https://msdn.microsoft.com/library/ms533809(v=VS.85).aspx">Recoloring</a>
 

 

