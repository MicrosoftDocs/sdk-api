---
UID: NF:dcomp.IDCompositionVisual.SetBitmapInterpolationMode
title: IDCompositionVisual::SetBitmapInterpolationMode
author: windows-sdk-content
description: Sets the BitmapInterpolationMode property, which specifies the mode for Microsoft DirectComposition to use when interpolating pixels from bitmaps that are not axis-aligned or drawn exactly at scale.
old-location: directcomp\idcompositionvisual_setbitmapinterpolationmode.htm
tech.root: directcomp
ms.assetid: F45A3619-556B-4D2C-BCB0-8D55A1397579
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDCompositionVisual interface [DirectComposition],SetBitmapInterpolationMode method, IDCompositionVisual.SetBitmapInterpolationMode, IDCompositionVisual::SetBitmapInterpolationMode, SetBitmapInterpolationMode, SetBitmapInterpolationMode method [DirectComposition], SetBitmapInterpolationMode method [DirectComposition],IDCompositionVisual interface, dcomp/IDCompositionVisual::SetBitmapInterpolationMode, directcomp.idcompositionvisual_setbitmapinterpolationmode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionVisual.SetBitmapInterpolationMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionVisual::SetBitmapInterpolationMode


## -description


Sets the BitmapInterpolationMode property, which specifies the mode for Microsoft DirectComposition to use when interpolating pixels from bitmaps that are not axis-aligned or drawn exactly at scale. 


## -parameters




### -param interpolationMode [in]

Type: <b><a href="https://msdn.microsoft.com/0B919A5C-DEDD-4131-B743-A61CA49CA2B6">DCOMPOSITION_BITMAP_INTERPOLATION_MODE</a></b>

The interpolation mode to use.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



The interpolation mode affects how a bitmap is composed when it is transformed such that there is no one-to-one correspondence between pixels in the bitmap and pixels on the screen.



By default, a visual inherits the interpolation mode of the parent visual, which may inherit the interpolation mode of its parent visual, and so on. A visual uses the default interpolation mode if this method is never called for the visual, or if this method is called with <a href="https://msdn.microsoft.com/en-us/library/Hh437364(v=VS.85).aspx">DCOMPOSITION_BITMAP_INTERPOLATION_MODE_INHERIT</a>. If no visuals set the interpolation mode, the default for the entire visual tree is nearest neighbor interpolation, which offers the lowest visual quality but the highest performance.



If the <i>interpolationMode</i> parameter is anything other than <a href="https://msdn.microsoft.com/en-us/library/Hh437364(v=VS.85).aspx">DCOMPOSITION_BITMAP_INTERPOLATION_MODE_INHERIT</a>, this visual's bitmap is composed with the specified interpolation mode, and this mode becomes the new default mode for the children of this visual. That is, if the interpolation mode of this visual's children is unchanged or explicitly set to <b>DCOMPOSITION_BITMAP_INTERPOLATION_MODE_INHERIT</b>, the bitmaps of the child visuals are composed using the interpolation mode of this visual.





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh449139(v=VS.85).aspx">IDCompositionVisual</a>
 

 

