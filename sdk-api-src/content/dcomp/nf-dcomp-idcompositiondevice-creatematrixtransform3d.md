---
UID: NF:dcomp.IDCompositionDevice.CreateMatrixTransform3D
title: IDCompositionDevice::CreateMatrixTransform3D (dcomp.h)
description: Creates a 3D 4-by-4 matrix transform object. (IDCompositionDevice.CreateMatrixTransform3D)
helpviewer_keywords: ["CreateMatrixTransform3D","CreateMatrixTransform3D method [DirectComposition]","CreateMatrixTransform3D method [DirectComposition]","IDCompositionDevice interface","IDCompositionDevice interface [DirectComposition]","CreateMatrixTransform3D method","IDCompositionDevice.CreateMatrixTransform3D","IDCompositionDevice::CreateMatrixTransform3D","dcomp/IDCompositionDevice::CreateMatrixTransform3D","directcomp.idcompositiondevice_creatematrixtransform3d"]
old-location: directcomp\idcompositiondevice_creatematrixtransform3d.htm
tech.root: directcomp
ms.assetid: 699DB053-3897-43EC-92E2-BD45CE643130
ms.date: 12/05/2018
ms.keywords: CreateMatrixTransform3D, CreateMatrixTransform3D method [DirectComposition], CreateMatrixTransform3D method [DirectComposition],IDCompositionDevice interface, IDCompositionDevice interface [DirectComposition],CreateMatrixTransform3D method, IDCompositionDevice.CreateMatrixTransform3D, IDCompositionDevice::CreateMatrixTransform3D, dcomp/IDCompositionDevice::CreateMatrixTransform3D, directcomp.idcompositiondevice_creatematrixtransform3d
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
 - IDCompositionDevice::CreateMatrixTransform3D
 - dcomp/IDCompositionDevice::CreateMatrixTransform3D
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
 - IDCompositionDevice.CreateMatrixTransform3D
---

# IDCompositionDevice::CreateMatrixTransform3D


## -description

Creates a 3D 4-by-4 matrix transform object.

## -parameters

### -param matrixTransform3D [out]

Type: <b><a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionmatrixtransform3d">IDCompositionMatrixTransform3D</a>**</b>

The new 3D matrix transform object. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

The new 3D matrix transform has the identity matrix as its value. The identity matrix is the 4-by-4 matrix with ones on the main diagonal and zeros elsewhere, as shown in the following illustration. 

<img alt="Four-by-four identity matrix" src="./images/identity_4x4matrix.png"/>

When an identity transform is applied to an object, it does not change the position, shape, or size of the object. It is similar to the way that multiplying a number by one does not change the number. Any transform other than the identity transform will modify the position, shape, and/or size of objects.

## -see-also

<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositioneffectgroup-settransform3d">DCompositionEffectGroup::SetTransform3D</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a>
