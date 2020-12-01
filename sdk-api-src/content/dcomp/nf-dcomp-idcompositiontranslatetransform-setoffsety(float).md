---
UID: NF:dcomp.IDCompositionTranslateTransform.SetOffsetY(float)
title: IDCompositionTranslateTransform::SetOffsetY (dcomp.h)
description: Changes the value of the OffsetY property of a 2D translation transform.
helpviewer_keywords: ["IDCompositionTranslateTransform interface [DirectComposition]","SetOffsetY method","IDCompositionTranslateTransform.SetOffsetY","IDCompositionTranslateTransform::SetOffsetY","IDCompositionTranslateTransform::SetOffsetY(float)","SetOffsetY","SetOffsetY method [DirectComposition]","SetOffsetY method [DirectComposition]","IDCompositionTranslateTransform interface","dcomp/IDCompositionTranslateTransform::SetOffsetY","directcomp.idcompositiontranslatetransform_setoffsety_float"]
old-location: directcomp\idcompositiontranslatetransform_setoffsety_float.htm
tech.root: directcomp
ms.assetid: 7EF80FFC-FB9B-4F4D-A321-7871E6C2E757
ms.date: 12/05/2018
ms.keywords: IDCompositionTranslateTransform interface [DirectComposition],SetOffsetY method, IDCompositionTranslateTransform.SetOffsetY, IDCompositionTranslateTransform::SetOffsetY, IDCompositionTranslateTransform::SetOffsetY(float), SetOffsetY, SetOffsetY method [DirectComposition], SetOffsetY method [DirectComposition],IDCompositionTranslateTransform interface, dcomp/IDCompositionTranslateTransform::SetOffsetY, directcomp.idcompositiontranslatetransform_setoffsety_float
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
 - IDCompositionTranslateTransform::SetOffsetY
 - dcomp/IDCompositionTranslateTransform::SetOffsetY
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
 - IDCompositionTranslateTransform.SetOffsetY
---

# IDCompositionTranslateTransform::SetOffsetY


## -description

Changes the value of the OffsetY property of a 2D translation transform. The OffsetY property specifies the distance to translate along the y-axis.

## -parameters

### -param offsetY [in]

Type: <b>float</b>

The distance to translate along the y-axis, in pixels.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

This method fails if the <i>offsetY</i> parameter is NaN, positive infinity, or negative infinity.



If the OffsetY property was previously animated, this method removes the animation and sets the OffsetY property to the specified static value.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontranslatetransform">IDCompositionTranslateTransform</a>



<a href="/previous-versions/windows/desktop/legacy/hh449126(v=vs.85)">IDCompositionTranslateTransform::SetOffsetX</a>