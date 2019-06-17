---
UID: NF:dcomp.IDCompositionColorMatrixEffect.SetMatrix
title: IDCompositionColorMatrixEffect::SetMatrix (dcomp.h)
author: windows-sdk-content
description: Sets the matrix used by the effect to multiply the RGBA values of the image.
old-location: directcomp\idcompositioncolormatrixeffect_setmatrix.htm
tech.root: directcomp
ms.assetid: 1EE0C9B6-6309-40A3-AE80-A47C45BBA536
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDCompositionColorMatrixEffect interface [DirectComposition],SetMatrix method, IDCompositionColorMatrixEffect.SetMatrix, IDCompositionColorMatrixEffect::SetMatrix, SetMatrix, SetMatrix method [DirectComposition], SetMatrix method [DirectComposition],IDCompositionColorMatrixEffect interface, dcomp/IDCompositionColorMatrixEffect::SetMatrix, directcomp.idcompositioncolormatrixeffect_setmatrix
ms.topic: method
f1_keywords: ["dcomp/IDCompositionColorMatrixEffect.SetMatrix"]
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IDCompositionColorMatrixEffect.SetMatrix
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionColorMatrixEffect::SetMatrix


## -description


Sets the matrix used by the effect to multiply the RGBA values of the image.


## -parameters




### -param matrix [in, ref]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/Direct2D/d2d1-matrix-5x4-f">D2D1_MATRIX_5X4_F</a></b>

The matrix used by the effect to multiply the RGBA values of the image. The matrix is column major and is applied as shown in the following equation:
          

<img alt="Matrix equation" src="./images/color_matrix_formula.png"/>

## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositioncolormatrixeffect">IDCompositionColorMatrixEffect</a>
 

 

