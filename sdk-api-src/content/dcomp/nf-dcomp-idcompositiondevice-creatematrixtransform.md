---
UID: NF:dcomp.IDCompositionDevice.CreateMatrixTransform
title: IDCompositionDevice::CreateMatrixTransform (dcomp.h)
description: Creates a 2D 3-by-2 matrix transform object. (IDCompositionDevice.CreateMatrixTransform)
helpviewer_keywords: ["CreateMatrixTransform","CreateMatrixTransform method [DirectComposition]","CreateMatrixTransform method [DirectComposition]","IDCompositionDevice interface","IDCompositionDevice interface [DirectComposition]","CreateMatrixTransform method","IDCompositionDevice.CreateMatrixTransform","IDCompositionDevice::CreateMatrixTransform","dcomp/IDCompositionDevice::CreateMatrixTransform","directcomp.idcompositiondevice_creatematrixtransform"]
old-location: directcomp\idcompositiondevice_creatematrixtransform.htm
tech.root: directcomp
ms.assetid: 79291366-2fb2-4130-a642-4993648d8aa6
ms.date: 12/05/2018
ms.keywords: CreateMatrixTransform, CreateMatrixTransform method [DirectComposition], CreateMatrixTransform method [DirectComposition],IDCompositionDevice interface, IDCompositionDevice interface [DirectComposition],CreateMatrixTransform method, IDCompositionDevice.CreateMatrixTransform, IDCompositionDevice::CreateMatrixTransform, dcomp/IDCompositionDevice::CreateMatrixTransform, directcomp.idcompositiondevice_creatematrixtransform
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
 - IDCompositionDevice::CreateMatrixTransform
 - dcomp/IDCompositionDevice::CreateMatrixTransform
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
 - IDCompositionDevice.CreateMatrixTransform
---

# IDCompositionDevice::CreateMatrixTransform


## -description

Creates a 2D 3-by-2 matrix transform object.

## -parameters

### -param matrixTransform [out]

Type: <b><a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionmatrixtransform">IDCompositionMatrixTransform</a>**</b>

The new matrix transform object. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

A new matrix transform object has the identity matrix as its initial value. The identity matrix is the 3x2 matrix with ones on the main diagonal and zeros elsewhere, as shown in the following illustration. 

<img alt="Three-by-two identity matrix" src="./images/identity_3x2matrix.png"/>

When an identity transform is applied to an object, it does not change the position, shape, or size of the object. It is similar to the way that multiplying a number by one does not change the number. Any transform other than the identity transform will modify the position, shape, and/or size of objects.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a>



<a href="/previous-versions/windows/desktop/legacy/hh449178(v=vs.85)">IDCompositionVisual::SetTransform</a>
