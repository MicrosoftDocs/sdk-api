---
UID: NF:dcomp.IDCompositionRotateTransform.SetCenterY(float)
title: IDCompositionRotateTransform::SetCenterY (dcomp.h)
description: Changes the value of the CenterY property of a 2D rotation transform.
helpviewer_keywords: ["IDCompositionRotateTransform interface [DirectComposition]","SetCenterY method","IDCompositionRotateTransform.SetCenterY","IDCompositionRotateTransform::SetCenterY","IDCompositionRotateTransform::SetCenterY(float)","SetCenterY","SetCenterY method [DirectComposition]","SetCenterY method [DirectComposition]","IDCompositionRotateTransform interface","dcomp/IDCompositionRotateTransform::SetCenterY","directcomp.idcompositionrotatetransform_setcentery_float"]
old-location: directcomp\idcompositionrotatetransform_setcentery_float.htm
tech.root: directcomp
ms.assetid: 7D4EF6C3-A0BA-42C4-841C-A40EEF5122F5
ms.date: 12/05/2018
ms.keywords: IDCompositionRotateTransform interface [DirectComposition],SetCenterY method, IDCompositionRotateTransform.SetCenterY, IDCompositionRotateTransform::SetCenterY, IDCompositionRotateTransform::SetCenterY(float), SetCenterY, SetCenterY method [DirectComposition], SetCenterY method [DirectComposition],IDCompositionRotateTransform interface, dcomp/IDCompositionRotateTransform::SetCenterY, directcomp.idcompositionrotatetransform_setcentery_float
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
 - IDCompositionRotateTransform::SetCenterY
 - dcomp/IDCompositionRotateTransform::SetCenterY
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
 - IDCompositionRotateTransform.SetCenterY
---

# IDCompositionRotateTransform::SetCenterY


## -description

Changes the value of the CenterY property of a 2D rotation transform. The CenterY property specifies the y-coordinate of the point about which the rotation is performed.

## -parameters

### -param centerY [in]

Type: <b>float</b>

The new y-coordinate of the center point.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

This method fails if the <i>centerY</i> parameter is NaN, positive infinity, or negative infinity.



If the CenterY property was previously animated, this method removes the animation and sets the CenterY property to the specified static value.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionrotatetransform">IDCompositionRotateTransform</a>



<a href="/previous-versions/windows/desktop/legacy/hh448982(v=vs.85)">IDCompositionRotateTransform::SetCenterX</a>