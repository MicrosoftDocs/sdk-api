---
UID: NF:dcomp.IDCompositionVisual3.SetTransform(constD2D_MATRIX_4X4_F&)
title: IDCompositionVisual3::SetTransform (dcomp.h)
description: Sets the Transform property of this visual to the specified 4-by-4 transform matrix.
helpviewer_keywords: ["IDCompositionVisual3 interface [DirectComposition]","SetTransform method","IDCompositionVisual3.SetTransform","IDCompositionVisual3::SetTransform","IDCompositionVisual3::SetTransform(const D2D_MATRIX_4X4_F &)","IDCompositionVisual3::SetTransform(const D2D_MATRIX_4X4_F&)","SetTransform","SetTransform method [DirectComposition]","SetTransform method [DirectComposition]","IDCompositionVisual3 interface","dcomp/IDCompositionVisual3::SetTransform","directcomp.idcompositionvisual3_settransform_1"]
old-location: directcomp\idcompositionvisual3_settransform_1.htm
tech.root: directcomp
ms.assetid: 1deb9c84-1a5b-5dac-af0f-ae6b49a9c473
ms.date: 12/05/2018
ms.keywords: IDCompositionVisual3 interface [DirectComposition],SetTransform method, IDCompositionVisual3.SetTransform, IDCompositionVisual3::SetTransform, IDCompositionVisual3::SetTransform(const D2D_MATRIX_4X4_F &), IDCompositionVisual3::SetTransform(const D2D_MATRIX_4X4_F&), SetTransform, SetTransform method [DirectComposition], SetTransform method [DirectComposition],IDCompositionVisual3 interface, dcomp/IDCompositionVisual3::SetTransform, directcomp.idcompositionvisual3_settransform_1
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
 - IDCompositionVisual3::SetTransform
 - dcomp/IDCompositionVisual3::SetTransform
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
 - IDCompositionVisual3.SetTransform
---

# IDCompositionVisual3::SetTransform


## -description

Sets the Transform property of this visual to the specified 4-by-4 transform matrix.

## -parameters

### -param matrix [in, ref]

Type: <b>const <a href="/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f">D2D_MATRIX_4X4_F</a></b>

The 4-by-4 transform matrix that is used to modify  the coordinate system of this visual.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

Setting the Transform property transforms the coordinate system of the entire visual subtree that is rooted at this visual. If the Clip property of this visual is specified, the clip rectangle is also transformed.



If the Transform property previously specified a transform object, the newly specified transform matrix replaces the transform object.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionmatrixtransform">IDCompositionMatrixTransform</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionrotatetransform">IDCompositionRotateTransform</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionscaletransform">IDCompositionScaleTransform</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionskewtransform">IDCompositionSkewTransform</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontransform">IDCompositionTransform</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontranslatetransform">IDCompositionTranslateTransform</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionvisual">IDCompositionVisual</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionvisual3">IDCompositionVisual3</a>



<a href="/previous-versions/windows/desktop/legacy/hh449165(v=vs.85)">IDCompositionVisual::SetOffsetX</a>



<a href="/previous-versions/windows/desktop/legacy/hh449171(v=vs.85)">IDCompositionVisual::SetOffsetY</a>