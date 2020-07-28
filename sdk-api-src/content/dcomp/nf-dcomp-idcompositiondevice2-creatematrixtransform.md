---
UID: NF:dcomp.IDCompositionDevice2.CreateMatrixTransform
title: IDCompositionDevice2::CreateMatrixTransform (dcomp.h)
description: Creates a 2D 3-by-2 matrix transform object.
helpviewer_keywords: ["CreateMatrixTransform","CreateMatrixTransform method [DirectComposition]","CreateMatrixTransform method [DirectComposition]","IDCompositionDevice2 interface","IDCompositionDevice2 interface [DirectComposition]","CreateMatrixTransform method","IDCompositionDevice2.CreateMatrixTransform","IDCompositionDevice2::CreateMatrixTransform","dcomp/IDCompositionDevice2::CreateMatrixTransform","directcomp.idcompositiondevice2_creatematrixtransform"]
old-location: directcomp\idcompositiondevice2_creatematrixtransform.htm
tech.root: directcomp
ms.assetid: 4E8D8560-F7D3-4075-A4E9-00AFCEB526BE
ms.date: 12/05/2018
ms.keywords: CreateMatrixTransform, CreateMatrixTransform method [DirectComposition], CreateMatrixTransform method [DirectComposition],IDCompositionDevice2 interface, IDCompositionDevice2 interface [DirectComposition],CreateMatrixTransform method, IDCompositionDevice2.CreateMatrixTransform, IDCompositionDevice2::CreateMatrixTransform, dcomp/IDCompositionDevice2::CreateMatrixTransform, directcomp.idcompositiondevice2_creatematrixtransform
f1_keywords:
- dcomp/IDCompositionDevice2.CreateMatrixTransform
dev_langs:
- c++
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
- IDCompositionDevice2.CreateMatrixTransform
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionDevice2::CreateMatrixTransform


## -description


Creates a 2D 3-by-2 matrix transform object.


## -parameters




### -param matrixTransform [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionmatrixtransform">IDCompositionMatrixTransform</a>**</b>

The new matrix transform object. This parameter must not be NULL.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://docs.microsoft.com/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



A new matrix transform object has the identity matrix as its initial value. The identity matrix is the 3x2 matrix with ones on the main diagonal and zeros elsewhere, as shown in the following illustration. 

<img alt="Three-by-two identity matrix" src="./images/identity_3x2matrix.png"/>

When an identity transform is applied to an object, it does not change the position, shape, or size of the object. It is similar to the way that multiplying a number by one does not change the number. Any transform other than the identity transform will modify the position, shape, and/or size of objects.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice2">IDCompositionDevice2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositioneffectgroup-settransform3d">IDCompositionEffectGroup::SetTransform3D</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-seteffect">IDCompositionVisual::SetEffect</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh449178(v=vs.85)">IDCompositionVisual::SetTransform</a>
 

 

