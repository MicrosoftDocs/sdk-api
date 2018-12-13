---
UID: NF:gdipluseffects.ColorMatrixEffect.GetParameters
title: ColorMatrixEffect::GetParameters
author: windows-sdk-content
description: The ColorMatrixEffect::GetParameters method gets the elements of the current 5x5 color matrix of this ColorMatrixEffect object.
old-location: gdiplus\_gdiplus_CLASS_ColorMatrixEffect_GetParameters_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\colormatrixeffectclass\colormatrixeffectmethods\getparameters.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
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
req.product: GDI+ 1.1
---

# ColorMatrixEffect::GetParameters


## -description


The <b>ColorMatrixEffect::GetParameters</b> method gets the elements of the current 5x5 color matrix of this <a href="https://msdn.microsoft.com/99a4a671-e128-4a1b-8c8a-e9231bd44e96">ColorMatrixEffect</a> object.


## -parameters




### -param size [in]

Type: <b>UINT*</b>

Pointer to a <b>UINT</b> that specifies the size, in bytes, of a <a href="https://msdn.microsoft.com/2b37702b-c87f-4f41-8240-a23393019ea3">ColorMatrix</a> structure.


### -param matrix [out]

Type: <b><a href="https://msdn.microsoft.com/2b37702b-c87f-4f41-8240-a23393019ea3">ColorMatrix</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/2b37702b-c87f-4f41-8240-a23393019ea3">ColorMatrix</a> structure that receives the elements of the color matrix.


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/99a4a671-e128-4a1b-8c8a-e9231bd44e96">ColorMatrixEffect</a>



<a href="https://msdn.microsoft.com/de649f16-eaf4-4af6-88d3-227aa01825e5">ColorMatrixEffect::SetParameters</a>
 

 

