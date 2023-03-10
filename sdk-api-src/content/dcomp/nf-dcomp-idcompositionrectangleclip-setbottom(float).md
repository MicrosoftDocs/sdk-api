---
UID: NF:dcomp.IDCompositionRectangleClip.SetBottom(float)
title: IDCompositionRectangleClip::SetBottom (dcomp.h)
description: Changes the value of the Bottom property of a clip object.
helpviewer_keywords: ["IDCompositionRectangleClip interface [DirectComposition]","SetBottom method","IDCompositionRectangleClip.SetBottom","IDCompositionRectangleClip::SetBottom","IDCompositionRectangleClip::SetBottom(float)","SetBottom","SetBottom method [DirectComposition]","SetBottom method [DirectComposition]","IDCompositionRectangleClip interface","dcomp/IDCompositionRectangleClip::SetBottom","directcomp.idcompositionrectangleclip_setbottom_float"]
old-location: directcomp\idcompositionrectangleclip_setbottom_float.htm
tech.root: directcomp
ms.assetid: BE07DF2B-6588-4ACD-8FB6-E467C9943710
ms.date: 12/05/2018
ms.keywords: IDCompositionRectangleClip interface [DirectComposition],SetBottom method, IDCompositionRectangleClip.SetBottom, IDCompositionRectangleClip::SetBottom, IDCompositionRectangleClip::SetBottom(float), SetBottom, SetBottom method [DirectComposition], SetBottom method [DirectComposition],IDCompositionRectangleClip interface, dcomp/IDCompositionRectangleClip::SetBottom, directcomp.idcompositionrectangleclip_setbottom_float
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
 - IDCompositionRectangleClip::SetBottom
 - dcomp/IDCompositionRectangleClip::SetBottom
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
 - IDCompositionRectangleClip.SetBottom
---

# IDCompositionRectangleClip::SetBottom


## -description

Changes the value of the Bottom property of a clip object. The Bottom property specifies the y-coordinate of the lower-right corner of the clip rectangle.

## -parameters

### -param bottom [in]

Type: <b>float</b>

The new value of the Bottom property, in pixels. This parameter has a numerical limit of -2^21 to 2^21. 
            The API accepts numbers outside of this range, but they are always clamped to this range.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. 
              See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

This method fails if the <i>bottom</i> parameter is NaN, positive infinity, or negative infinity.

      

If the Bottom property was previously animated, this method removes the animation and sets the Bottom property to the specified static value.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionrectangleclip">IDCompositionRectangleClip</a>