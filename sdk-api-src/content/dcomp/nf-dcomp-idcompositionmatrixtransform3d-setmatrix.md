---
UID: NF:dcomp.IDCompositionMatrixTransform3D.SetMatrix
title: IDCompositionMatrixTransform3D::SetMatrix (dcomp.h)
description: Changes all values of the matrix of this 3D transformation effect.
helpviewer_keywords: ["IDCompositionMatrixTransform3D interface [DirectComposition]","SetMatrix method","IDCompositionMatrixTransform3D.SetMatrix","IDCompositionMatrixTransform3D::SetMatrix","SetMatrix","SetMatrix method [DirectComposition]","SetMatrix method [DirectComposition]","IDCompositionMatrixTransform3D interface","dcomp/IDCompositionMatrixTransform3D::SetMatrix","directcomp.idcompositionmatrixtransform3d_setmatrix"]
old-location: directcomp\idcompositionmatrixtransform3d_setmatrix.htm
tech.root: directcomp
ms.assetid: 0F1DBC1C-154A-4785-B9B9-924353FD5836
ms.date: 12/05/2018
ms.keywords: IDCompositionMatrixTransform3D interface [DirectComposition],SetMatrix method, IDCompositionMatrixTransform3D.SetMatrix, IDCompositionMatrixTransform3D::SetMatrix, SetMatrix, SetMatrix method [DirectComposition], SetMatrix method [DirectComposition],IDCompositionMatrixTransform3D interface, dcomp/IDCompositionMatrixTransform3D::SetMatrix, directcomp.idcompositionmatrixtransform3d_setmatrix
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
 - IDCompositionMatrixTransform3D::SetMatrix
 - dcomp/IDCompositionMatrixTransform3D::SetMatrix
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
 - IDCompositionMatrixTransform3D.SetMatrix
---

# IDCompositionMatrixTransform3D::SetMatrix


## -description

Changes all values of the matrix of this 3D transformation effect.

## -parameters

### -param matrix [ref]

Type: <b>const <a href="/windows/desktop/direct3d9/d3dmatrix">D3DMATRIX</a></b>

The new matrix for this 3D transformation effect.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

This method fails if any of the matrix values are NaN, positive infinity, or negative infinity.

If any of the matrix elements were previously animated, this method removes the animations and sets the elements to the specified static value.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionmatrixtransform3d">IDCompositionMatrixTransform3D</a>