---
UID: NF:gdipluseffects.ColorMatrixEffect.GetParameters
title: ColorMatrixEffect::GetParameters
author: windows-sdk-content
description: The ColorMatrixEffect::GetParameters method gets the elements of the current 5x5 color matrix of this ColorMatrixEffect object.
old-location: gdiplus\_gdiplus_CLASS_ColorMatrixEffect_GetParameters_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\colormatrixeffectclass\colormatrixeffectmethods\getparameters.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ColorMatrixEffect class [GDI+],GetParameters method, ColorMatrixEffect.GetParameters, ColorMatrixEffect::GetParameters, GetParameters, GetParameters method [GDI+], GetParameters method [GDI+],ColorMatrixEffect class, _gdiplus_CLASS_ColorMatrixEffect_GetParameters_, gdiplus._gdiplus_CLASS_ColorMatrixEffect_GetParameters_
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
 - ColorMatrixEffect.GetParameters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- gdipluseffects.h
: 
- ColorMatrixEffect.GetParameters
: 
req.product: GDI+ 1.1
---

# ColorMatrixEffect::GetParameters


## -description


The <b>ColorMatrixEffect::GetParameters</b> method gets the elements of the current 5x5 color matrix of this <a href="https://msdn.microsoft.com/en-us/library/ms534431(v=VS.85).aspx">ColorMatrixEffect</a> object.


## -parameters




### -param size [in]

Type: <b>UINT*</b>

Pointer to a <b>UINT</b> that specifies the size, in bytes, of a <a href="https://msdn.microsoft.com/en-us/library/ms534063(v=VS.85).aspx">ColorMatrix</a> structure.


### -param matrix [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534063(v=VS.85).aspx">ColorMatrix</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534063(v=VS.85).aspx">ColorMatrix</a> structure that receives the elements of the color matrix.


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534431(v=VS.85).aspx">ColorMatrixEffect</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536233(v=VS.85).aspx">ColorMatrixEffect::SetParameters</a>
 

 

