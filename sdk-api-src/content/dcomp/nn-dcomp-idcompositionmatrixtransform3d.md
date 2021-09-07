---
UID: NN:dcomp.IDCompositionMatrixTransform3D
title: IDCompositionMatrixTransform3D (dcomp.h)
description: Represents an arbitrary 3D transformation defined by a 4-by-4 matrix.
helpviewer_keywords: ["IDCompositionMatrixTransform3D","IDCompositionMatrixTransform3D interface [DirectComposition]","IDCompositionMatrixTransform3D interface [DirectComposition]","described","dcomp/IDCompositionMatrixTransform3D","directcomp.idcompositionmatrixtransform3d"]
old-location: directcomp\idcompositionmatrixtransform3d.htm
tech.root: directcomp
ms.assetid: 56C9A564-2504-4940-B850-D280C8E0CF82
ms.date: 12/05/2018
ms.keywords: IDCompositionMatrixTransform3D, IDCompositionMatrixTransform3D interface [DirectComposition], IDCompositionMatrixTransform3D interface [DirectComposition],described, dcomp/IDCompositionMatrixTransform3D, directcomp.idcompositionmatrixtransform3d
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
 - IDCompositionMatrixTransform3D
 - dcomp/IDCompositionMatrixTransform3D
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
 - IDCompositionMatrixTransform3D
---

# IDCompositionMatrixTransform3D interface


## -description

Represents an arbitrary 3D transformation defined by a 4-by-4 matrix.

## -inheritance

The <b>IDCompositionMatrixTransform3D</b> interface inherits from <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontransform3d">IDCompositionTransform3D</a>. <b>IDCompositionMatrixTransform3D</b> also has these types of members:

## -remarks

A 3D matrix transform represents the following 4-by-4 matrix:

<img alt="Four-by-four 3D transform matrix" src="./images/3D_matrix.png"/>

 The application can set any of the values in the first three columns. Note that the fourth column is padded to allow for matrix concatenation.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontransform3d">IDCompositionTransform3D</a>



<a href="/previous-versions/windows/desktop/legacy/hh449178(v=vs.85)">IDCompositionVisual::SetTransform</a>
