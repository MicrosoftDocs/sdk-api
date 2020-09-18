---
UID: NF:dcomp.IDCompositionVisual.SetBitmapInterpolationMode
title: IDCompositionVisual::SetBitmapInterpolationMode (dcomp.h)
description: Sets the BitmapInterpolationMode property, which specifies the mode for Microsoft DirectComposition to use when interpolating pixels from bitmaps that are not axis-aligned or drawn exactly at scale.
helpviewer_keywords: ["IDCompositionVisual interface [DirectComposition]","SetBitmapInterpolationMode method","IDCompositionVisual.SetBitmapInterpolationMode","IDCompositionVisual::SetBitmapInterpolationMode","SetBitmapInterpolationMode","SetBitmapInterpolationMode method [DirectComposition]","SetBitmapInterpolationMode method [DirectComposition]","IDCompositionVisual interface","dcomp/IDCompositionVisual::SetBitmapInterpolationMode","directcomp.idcompositionvisual_setbitmapinterpolationmode"]
old-location: directcomp\idcompositionvisual_setbitmapinterpolationmode.htm
tech.root: directcomp
ms.assetid: F45A3619-556B-4D2C-BCB0-8D55A1397579
ms.date: 12/05/2018
ms.keywords: IDCompositionVisual interface [DirectComposition],SetBitmapInterpolationMode method, IDCompositionVisual.SetBitmapInterpolationMode, IDCompositionVisual::SetBitmapInterpolationMode, SetBitmapInterpolationMode, SetBitmapInterpolationMode method [DirectComposition], SetBitmapInterpolationMode method [DirectComposition],IDCompositionVisual interface, dcomp/IDCompositionVisual::SetBitmapInterpolationMode, directcomp.idcompositionvisual_setbitmapinterpolationmode
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDCompositionVisual::SetBitmapInterpolationMode
 - dcomp/IDCompositionVisual::SetBitmapInterpolationMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionVisual.SetBitmapInterpolationMode
---

# IDCompositionVisual::SetBitmapInterpolationMode


## -description

Sets the BitmapInterpolationMode property, which specifies the mode for Microsoft DirectComposition to use when interpolating pixels from bitmaps that are not axis-aligned or drawn exactly at scale.

## -parameters

### -param interpolationMode [in]

Type: <b><a href="/windows/desktop/api/dcomptypes/ne-dcomptypes-dcomposition_bitmap_interpolation_mode">DCOMPOSITION_BITMAP_INTERPOLATION_MODE</a></b>

The interpolation mode to use.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

The interpolation mode affects how a bitmap is composed when it is transformed such that there is no one-to-one correspondence between pixels in the bitmap and pixels on the screen.



By default, a visual inherits the interpolation mode of the parent visual, which may inherit the interpolation mode of its parent visual, and so on. A visual uses the default interpolation mode if this method is never called for the visual, or if this method is called with <a href="/windows/desktop/api/dcomptypes/ne-dcomptypes-dcomposition_bitmap_interpolation_mode">DCOMPOSITION_BITMAP_INTERPOLATION_MODE_INHERIT</a>. If no visuals set the interpolation mode, the default for the entire visual tree is nearest neighbor interpolation, which offers the lowest visual quality but the highest performance.



If the <i>interpolationMode</i> parameter is anything other than <a href="/windows/desktop/api/dcomptypes/ne-dcomptypes-dcomposition_bitmap_interpolation_mode">DCOMPOSITION_BITMAP_INTERPOLATION_MODE_INHERIT</a>, this visual's bitmap is composed with the specified interpolation mode, and this mode becomes the new default mode for the children of this visual. That is, if the interpolation mode of this visual's children is unchanged or explicitly set to <b>DCOMPOSITION_BITMAP_INTERPOLATION_MODE_INHERIT</b>, the bitmaps of the child visuals are composed using the interpolation mode of this visual.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionvisual">IDCompositionVisual</a>