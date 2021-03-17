---
UID: NF:dcomp.IDCompositionScaleTransform.SetCenterY(float)
title: IDCompositionScaleTransform::SetCenterY (dcomp.h)
description: Changes the value of the CenterY property of a 2D scale transform.
helpviewer_keywords: ["IDCompositionScaleTransform interface [DirectComposition]","SetCenterY method","IDCompositionScaleTransform.SetCenterY","IDCompositionScaleTransform::SetCenterY","IDCompositionScaleTransform::SetCenterY(float)","SetCenterY","SetCenterY method [DirectComposition]","SetCenterY method [DirectComposition]","IDCompositionScaleTransform interface","dcomp/IDCompositionScaleTransform::SetCenterY","directcomp.idcompositionscaletransform_setcentery_float"]
old-location: directcomp\idcompositionscaletransform_setcentery_float.htm
tech.root: directcomp
ms.assetid: 32E8FCBD-75D8-4162-9388-57B0348BD46B
ms.date: 12/05/2018
ms.keywords: IDCompositionScaleTransform interface [DirectComposition],SetCenterY method, IDCompositionScaleTransform.SetCenterY, IDCompositionScaleTransform::SetCenterY, IDCompositionScaleTransform::SetCenterY(float), SetCenterY, SetCenterY method [DirectComposition], SetCenterY method [DirectComposition],IDCompositionScaleTransform interface, dcomp/IDCompositionScaleTransform::SetCenterY, directcomp.idcompositionscaletransform_setcentery_float
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
 - IDCompositionScaleTransform::SetCenterY
 - dcomp/IDCompositionScaleTransform::SetCenterY
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
 - IDCompositionScaleTransform.SetCenterY
---

# IDCompositionScaleTransform::SetCenterY


## -description

Changes the value of the CenterY property of a 2D scale transform. The CenterY property specifies the y-coordinate of the point about which scaling is performed.

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

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionscaletransform">IDCompositionScaleTransform</a>



<a href="/previous-versions/windows/desktop/legacy/hh449036(v=vs.85)">IDCompositionScaleTransform::SetCenterX</a>