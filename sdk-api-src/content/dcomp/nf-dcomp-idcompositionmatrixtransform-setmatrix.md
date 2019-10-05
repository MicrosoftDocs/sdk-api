---
UID: NF:dcomp.IDCompositionMatrixTransform.SetMatrix
title: IDCompositionMatrixTransform::SetMatrix (dcomp.h)
author: windows-sdk-content
description: Changes all values of the matrix of this 2D transform.
old-location: directcomp\idcompositionmatrixtransform_setmatrix.htm
tech.root: directcomp
ms.assetid: 1f164dfd-8bd4-4f6e-a5d2-d455808b5b0f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDCompositionMatrixTransform interface [DirectComposition],SetMatrix method, IDCompositionMatrixTransform.SetMatrix, IDCompositionMatrixTransform::SetMatrix, SetMatrix, SetMatrix method [DirectComposition], SetMatrix method [DirectComposition],IDCompositionMatrixTransform interface, dcomp/IDCompositionMatrixTransform::SetMatrix, directcomp.idcompositionmatrixtransform_setmatrix
ms.topic: method
f1_keywords: 
 - "dcomp/IDCompositionMatrixTransform.SetMatrix"
dev_langs:
 - c++
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
 - IDCompositionMatrixTransform.SetMatrix
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionMatrixTransform::SetMatrix


## -description


Changes all values of the matrix of this 2D transform.


## -parameters




### -param matrix [ref]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f">D2D_MATRIX_3X2_F</a></b>

The new matrix for this 2D transform.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://docs.microsoft.com/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method fails if any of the matrix values are NaN, positive infinity, or negative infinity.

If any of the matrix elements were previously animated, this method removes the animations and sets the elements to the specified static value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionmatrixtransform">IDCompositionMatrixTransform</a>
 

 

