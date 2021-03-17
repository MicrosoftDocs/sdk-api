---
UID: NF:dcomp.IDCompositionRectangleClip.SetTop(float)
title: IDCompositionRectangleClip::SetTop (dcomp.h)
description: Changes the value of the Top property of a clip rectangle.
helpviewer_keywords: ["IDCompositionRectangleClip interface [DirectComposition]","SetTop method","IDCompositionRectangleClip.SetTop","IDCompositionRectangleClip::SetTop","IDCompositionRectangleClip::SetTop(float)","SetTop","SetTop method [DirectComposition]","SetTop method [DirectComposition]","IDCompositionRectangleClip interface","dcomp/IDCompositionRectangleClip::SetTop","directcomp.idcompositionrectangleclip_settop_float"]
old-location: directcomp\idcompositionrectangleclip_settop_float.htm
tech.root: directcomp
ms.assetid: 7D3AB5CC-7295-4160-9AAB-91C61A445B24
ms.date: 12/05/2018
ms.keywords: IDCompositionRectangleClip interface [DirectComposition],SetTop method, IDCompositionRectangleClip.SetTop, IDCompositionRectangleClip::SetTop, IDCompositionRectangleClip::SetTop(float), SetTop, SetTop method [DirectComposition], SetTop method [DirectComposition],IDCompositionRectangleClip interface, dcomp/IDCompositionRectangleClip::SetTop, directcomp.idcompositionrectangleclip_settop_float
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
 - IDCompositionRectangleClip::SetTop
 - dcomp/IDCompositionRectangleClip::SetTop
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
 - IDCompositionRectangleClip.SetTop
---

# IDCompositionRectangleClip::SetTop


## -description

Changes the value of the Top property of a clip rectangle. The Top property specifies the y-coordinate of the upper-left corner of the clip rectangle.

## -parameters

### -param top [in]

Type: <b>float</b>

The new value of the Top property, in pixels. This parameter has a numerical limit of -2^21 to 2^21. 
            The API accepts numbers outside of this range, but they are always clamped to this range.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

This method fails if the <i>top</i> parameter is NaN, positive infinity, or negative infinity.

      

If the Top property was previously animated, this method removes the animation and sets the Top property to the specified static value.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionrectangleclip">IDCompositionRectangleClip</a>