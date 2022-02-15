---
UID: NF:dcomp.IDCompositionTranslateTransform.SetOffsetX(float)
title: IDCompositionTranslateTransform::SetOffsetX(float) (dcomp.h)
description: Changes the value of the OffsetX property of a 2D translation transform.
helpviewer_keywords: ["IDCompositionTranslateTransform interface [DirectComposition]","SetOffsetX method","IDCompositionTranslateTransform.SetOffsetX","IDCompositionTranslateTransform.SetOffsetX(float)","IDCompositionTranslateTransform::SetOffsetX","IDCompositionTranslateTransform::SetOffsetX(float)","SetOffsetX","SetOffsetX method [DirectComposition]","SetOffsetX method [DirectComposition]","IDCompositionTranslateTransform interface","dcomp/IDCompositionTranslateTransform::SetOffsetX","directcomp.idcompositiontranslatetransform_setoffsetx_float"]
old-location: directcomp\idcompositiontranslatetransform_setoffsetx_float.htm
tech.root: directcomp
ms.assetid: F5D96E02-2FB0-45AD-8F4A-8FB955A40C3F
ms.date: 12/05/2018
ms.keywords: IDCompositionTranslateTransform interface [DirectComposition],SetOffsetX method, IDCompositionTranslateTransform.SetOffsetX, IDCompositionTranslateTransform.SetOffsetX(float), IDCompositionTranslateTransform::SetOffsetX, IDCompositionTranslateTransform::SetOffsetX(float), SetOffsetX, SetOffsetX method [DirectComposition], SetOffsetX method [DirectComposition],IDCompositionTranslateTransform interface, dcomp/IDCompositionTranslateTransform::SetOffsetX, directcomp.idcompositiontranslatetransform_setoffsetx_float
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
 - IDCompositionTranslateTransform::SetOffsetX
 - dcomp/IDCompositionTranslateTransform::SetOffsetX
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
 - IDCompositionTranslateTransform.SetOffsetX
---

# IDCompositionTranslateTransform::SetOffsetX(float)


## -description

Changes the value of the OffsetX property of a 2D translation transform. The OffsetX property specifies the distance to translate along the x-axis.

## -parameters

### -param offsetX [in]

Type: <b>float</b>

 The distance to translate along the x-axis, in pixels.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

This method performs an affine transformation, which moves every point by a fixed distance in the same direction. It is similar to shifting the origin of the coordinate space. 

This method fails if the <i>offsetX</i> parameter is NaN, positive infinity, or negative infinity.



If the OffsetX property was previously animated, this method removes the animation and sets the OffsetX property to the specified static value.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontranslatetransform">IDCompositionTranslateTransform</a>



<a href="/previous-versions/windows/desktop/legacy/hh449131(v=vs.85)">IDCompositionTranslateTransform::SetOffsetY</a>