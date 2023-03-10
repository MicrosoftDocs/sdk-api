---
UID: NF:dcomp.IDCompositionRectangleClip.SetLeft(float)
title: IDCompositionRectangleClip::SetLeft(float) (dcomp.h)
description: Changes the value of the Left property of a clip rectangle.
helpviewer_keywords: ["IDCompositionRectangleClip interface [DirectComposition]","SetLeft method","IDCompositionRectangleClip.SetLeft","IDCompositionRectangleClip.SetLeft(float)","IDCompositionRectangleClip::SetLeft","IDCompositionRectangleClip::SetLeft(float)","SetLeft","SetLeft method [DirectComposition]","SetLeft method [DirectComposition]","IDCompositionRectangleClip interface","dcomp/IDCompositionRectangleClip::SetLeft","directcomp.idcompositionrectangleclip_setleft_float"]
old-location: directcomp\idcompositionrectangleclip_setleft_float.htm
tech.root: directcomp
ms.assetid: 56614B81-3AC7-484C-9049-5E189D1C0B3B
ms.date: 12/05/2018
ms.keywords: IDCompositionRectangleClip interface [DirectComposition],SetLeft method, IDCompositionRectangleClip.SetLeft, IDCompositionRectangleClip.SetLeft(float), IDCompositionRectangleClip::SetLeft, IDCompositionRectangleClip::SetLeft(float), SetLeft, SetLeft method [DirectComposition], SetLeft method [DirectComposition],IDCompositionRectangleClip interface, dcomp/IDCompositionRectangleClip::SetLeft, directcomp.idcompositionrectangleclip_setleft_float
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
 - IDCompositionRectangleClip::SetLeft
 - dcomp/IDCompositionRectangleClip::SetLeft
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
 - IDCompositionRectangleClip.SetLeft
---

# IDCompositionRectangleClip::SetLeft(float)


## -description

Changes the value of the Left property of a clip rectangle. The Left property specifies the x-coordinate of the upper-left corner of the clip rectangle.

## -parameters

### -param left [in]

Type: <b>float</b>

The new value of the Left property, in pixels. This parameter has a numerical limit of -2^21 to 2^21. 
            The API accepts numbers outside of this range, but they are always clamped to this range.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

This method fails if the <i>left</i> parameter is NaN, positive infinity, or negative infinity.

      

If the Left property was previously animated, this method removes the animation and sets the Left property to the specified static value.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionrectangleclip">IDCompositionRectangleClip</a>