---
UID: NF:dcomp.IDCompositionTranslateTransform3D.SetOffsetX(float)
title: IDCompositionTranslateTransform3D::SetOffsetX(float) (dcomp.h)
description: Changes the value of the OffsetX property of a 3D translation transform effect. The OffsetX property specifies the distance to translate along the x-axis.
helpviewer_keywords: ["IDCompositionTranslateTransform3D interface [DirectComposition]","SetOffsetX method","IDCompositionTranslateTransform3D.SetOffsetX","IDCompositionTranslateTransform3D.SetOffsetX(float)","IDCompositionTranslateTransform3D::SetOffsetX","IDCompositionTranslateTransform3D::SetOffsetX(float)","SetOffsetX","SetOffsetX method [DirectComposition]","SetOffsetX method [DirectComposition]","IDCompositionTranslateTransform3D interface","dcomp/IDCompositionTranslateTransform3D::SetOffsetX","directcomp.idcompositiontranslatetransform3d_setoffsetx_float"]
old-location: directcomp\idcompositiontranslatetransform3d_setoffsetx_float.htm
tech.root: directcomp
ms.assetid: 1C31C4B1-A31E-4131-A305-91AF4E6EF1B5
ms.date: 12/05/2018
ms.keywords: IDCompositionTranslateTransform3D interface [DirectComposition],SetOffsetX method, IDCompositionTranslateTransform3D.SetOffsetX, IDCompositionTranslateTransform3D.SetOffsetX(float), IDCompositionTranslateTransform3D::SetOffsetX, IDCompositionTranslateTransform3D::SetOffsetX(float), SetOffsetX, SetOffsetX method [DirectComposition], SetOffsetX method [DirectComposition],IDCompositionTranslateTransform3D interface, dcomp/IDCompositionTranslateTransform3D::SetOffsetX, directcomp.idcompositiontranslatetransform3d_setoffsetx_float
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
 - IDCompositionTranslateTransform3D::SetOffsetX
 - dcomp/IDCompositionTranslateTransform3D::SetOffsetX
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
 - IDCompositionTranslateTransform3D.SetOffsetX
---

# IDCompositionTranslateTransform3D::SetOffsetX(float)


## -description

Changes the value of the OffsetX property of a 3D translation transform effect. The OffsetX property specifies the distance to translate along the x-axis.

## -parameters

### -param offsetX [in]

Type: <b>float</b>

The distance to translate along the x-axis, in pixels.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

This method fails if the <i>offsetX</i> parameter is NaN, positive infinity, or negative infinity.



If the OffsetX property was previously animated, this method removes the animation and sets the OffsetX property to the specified static value.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontranslatetransform3d">IDCompositionTranslateTransform3D</a>



<a href="/windows/win32/api/dcomp/nf-dcomp-idcompositiontranslatetransform3d-setoffsety(float)">IDCompositionTranslateTransform3D::SetOffsetY</a>



<a href="/windows/win32/api/dcomp/nf-dcomp-idcompositiontranslatetransform3d-setoffsetz(float)">IDCompositionTranslateTransform3D::SetOffsetZ</a>