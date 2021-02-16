---
UID: NF:dcomp.IDCompositionRotateTransform.SetCenterX(float)
title: IDCompositionRotateTransform::SetCenterX (dcomp.h)
description: Changes the value of the CenterX property of a 2D rotation transform.
helpviewer_keywords: ["IDCompositionRotateTransform interface [DirectComposition]","SetCenterX method","IDCompositionRotateTransform.SetCenterX","IDCompositionRotateTransform::SetCenterX","IDCompositionRotateTransform::SetCenterX(float)","SetCenterX","SetCenterX method [DirectComposition]","SetCenterX method [DirectComposition]","IDCompositionRotateTransform interface","dcomp/IDCompositionRotateTransform::SetCenterX","directcomp.idcompositionrotatetransform_setcenterx_float"]
old-location: directcomp\idcompositionrotatetransform_setcenterx_float.htm
tech.root: directcomp
ms.assetid: A1E2E033-031E-4781-9FCC-DC3190CCAB61
ms.date: 12/05/2018
ms.keywords: IDCompositionRotateTransform interface [DirectComposition],SetCenterX method, IDCompositionRotateTransform.SetCenterX, IDCompositionRotateTransform::SetCenterX, IDCompositionRotateTransform::SetCenterX(float), SetCenterX, SetCenterX method [DirectComposition], SetCenterX method [DirectComposition],IDCompositionRotateTransform interface, dcomp/IDCompositionRotateTransform::SetCenterX, directcomp.idcompositionrotatetransform_setcenterx_float
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
 - IDCompositionRotateTransform::SetCenterX
 - dcomp/IDCompositionRotateTransform::SetCenterX
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
 - IDCompositionRotateTransform.SetCenterX
---

# IDCompositionRotateTransform::SetCenterX


## -description

Changes the value of the CenterX property of a 2D rotation transform. The CenterX property specifies the x-coordinate of the point about which the rotation is performed.

## -parameters

### -param centerX [in]

Type: <b>float</b>

The new x-coordinate of the center point.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

This method fails if the <i>centerX</i> parameter is NaN, positive infinity, or negative infinity.



If the CenterX property was previously animated, this method removes the animation and sets the CenterX property to the specified static value.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionrotatetransform">IDCompositionRotateTransform</a>



<a href="/previous-versions/windows/desktop/legacy/hh448988(v=vs.85)">IDCompositionRotateTransform::SetCenterY</a>