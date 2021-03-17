---
UID: NF:dcomp.IDCompositionScaleTransform3D.SetScaleX(float)
title: IDCompositionScaleTransform3D::SetScaleX(float) (dcomp.h)
description: Changes the value of the ScaleX property of a 3D scale transform.
helpviewer_keywords: ["IDCompositionScaleTransform3D interface [DirectComposition]","SetScaleX method","IDCompositionScaleTransform3D.SetScaleX","IDCompositionScaleTransform3D.SetScaleX(float)","IDCompositionScaleTransform3D::SetScaleX","IDCompositionScaleTransform3D::SetScaleX(float)","SetScaleX","SetScaleX method [DirectComposition]","SetScaleX method [DirectComposition]","IDCompositionScaleTransform3D interface","dcomp/IDCompositionScaleTransform3D::SetScaleX","directcomp.idcompositionscaletransform3d_setscalex_float"]
old-location: directcomp\idcompositionscaletransform3d_setscalex_float.htm
tech.root: directcomp
ms.assetid: 6461C857-AC6E-4F27-9DE2-F1B3E00846D8
ms.date: 12/05/2018
ms.keywords: IDCompositionScaleTransform3D interface [DirectComposition],SetScaleX method, IDCompositionScaleTransform3D.SetScaleX, IDCompositionScaleTransform3D.SetScaleX(float), IDCompositionScaleTransform3D::SetScaleX, IDCompositionScaleTransform3D::SetScaleX(float), SetScaleX, SetScaleX method [DirectComposition], SetScaleX method [DirectComposition],IDCompositionScaleTransform3D interface, dcomp/IDCompositionScaleTransform3D::SetScaleX, directcomp.idcompositionscaletransform3d_setscalex_float
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
 - IDCompositionScaleTransform3D::SetScaleX
 - dcomp/IDCompositionScaleTransform3D::SetScaleX
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
 - IDCompositionScaleTransform3D.SetScaleX
---

# IDCompositionScaleTransform3D::SetScaleX(float)


## -description

Changes the value of the ScaleX property of a 3D scale transform. The ScaleX property specifies the scale factor along the x-axis.

## -parameters

### -param scaleX [in]

Type: <b>float</b>

The new x-axis scale factor.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

This method fails if the <i>scaleX</i> parameter is NaN, positive infinity, or negative infinity.



If the ScaleX property was previously animated, this method removes the animation and sets the ScaleX property to the specified static value.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionscaletransform">IDCompositionScaleTransform3D</a>



<a href="/windows/win32/api/dcomp/nf-dcomp-idcompositionscaletransform3d-setscaley(float)">IDCompositionScaleTransform3D::SetScaleY</a>



<a href="/windows/win32/api/dcomp/nf-dcomp-idcompositionscaletransform3d-setscalez(float)">IDCompositionScaleTransform3D::SetScaleZ</a>