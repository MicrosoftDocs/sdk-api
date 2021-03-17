---
UID: NF:dcomp.IDCompositionRectangleClip.SetRight(float)
title: IDCompositionRectangleClip::SetRight (dcomp.h)
description: Changes the value of the Right property of a clip rectangle.
helpviewer_keywords: ["IDCompositionRectangleClip interface [DirectComposition]","SetRight method","IDCompositionRectangleClip.SetRight","IDCompositionRectangleClip::SetRight","IDCompositionRectangleClip::SetRight(float)","SetRight","SetRight method [DirectComposition]","SetRight method [DirectComposition]","IDCompositionRectangleClip interface","dcomp/IDCompositionRectangleClip::SetRight","directcomp.idcompositionrectangleclip_setright_float"]
old-location: directcomp\idcompositionrectangleclip_setright_float.htm
tech.root: directcomp
ms.assetid: FB27BB00-239A-42A8-86D3-C78E2E8E820B
ms.date: 12/05/2018
ms.keywords: IDCompositionRectangleClip interface [DirectComposition],SetRight method, IDCompositionRectangleClip.SetRight, IDCompositionRectangleClip::SetRight, IDCompositionRectangleClip::SetRight(float), SetRight, SetRight method [DirectComposition], SetRight method [DirectComposition],IDCompositionRectangleClip interface, dcomp/IDCompositionRectangleClip::SetRight, directcomp.idcompositionrectangleclip_setright_float
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
 - IDCompositionRectangleClip::SetRight
 - dcomp/IDCompositionRectangleClip::SetRight
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
 - IDCompositionRectangleClip.SetRight
---

# IDCompositionRectangleClip::SetRight


## -description

Changes the value of the Right property of a clip rectangle. The Right property specifies the x-coordinate of the lower-right corner of the clip rectangle.

## -parameters

### -param right [in]

Type: <b>float</b>

The new value of the Right property, in pixels. This parameter has a numerical limit of -2^21 to 2^21. 
            The API accepts numbers outside of this range, but they are always clamped to this range.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

This method fails if the <i>right</i> parameter is NaN, positive infinity, or negative infinity.

      

If the Right property was previously animated, this method removes the animation and sets the Right property to the specified static value.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionrectangleclip">IDCompositionRectangleClip</a>