---
UID: NF:dcompanimation.IDCompositionAnimation.End
title: IDCompositionAnimation::End (dcompanimation.h)
description: Adds an end segment that marks the end of an animation function.
helpviewer_keywords: ["End","End method [DirectComposition]","End method [DirectComposition]","IDCompositionAnimation interface","IDCompositionAnimation interface [DirectComposition]","End method","IDCompositionAnimation.End","IDCompositionAnimation::End","dcompanimation/IDCompositionAnimation::End","directcomp.idcompositionanimation_end"]
old-location: directcomp\idcompositionanimation_end.htm
tech.root: directcomp
ms.assetid: 71287ae2-d930-4e96-8c12-538d2b58ccc6
ms.date: 12/05/2018
ms.keywords: End, End method [DirectComposition], End method [DirectComposition],IDCompositionAnimation interface, IDCompositionAnimation interface [DirectComposition],End method, IDCompositionAnimation.End, IDCompositionAnimation::End, dcompanimation/IDCompositionAnimation::End, directcomp.idcompositionanimation_end
req.header: dcompanimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DcompAnimation.idl
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
 - IDCompositionAnimation::End
 - dcompanimation/IDCompositionAnimation::End
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
 - IDCompositionAnimation.End
---

# IDCompositionAnimation::End


## -description

Adds an end segment that marks the end of an animation function.

## -parameters

### -param endOffset [in]

Type: <b>double</b>

The offset, in seconds, from the beginning of the animation function to the point when the function ends.

### -param endValue [in]

Type: <b>float</b>

The final value of the animation.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

When the specified offset is reached, the property or properties affected by this animation are set to the specified final value, and then the animation stops. If no end segment is added, the final segment of the animation function runs indefinitely. Calling this method is semantically identical to making the last segment of the animation function a cubic polynomial where the cubic, quadratic, and linear coefficients are all zeros, and the constant coefficient is the desired final value.

Because animation segments must be added in increasing order, this method fails if the <i>endOffset</i> parameter is less than or equal to the <i>beginOffset</i> parameter of the previous segment. This method also fails if this is the first segment to be added to the animation function.

After this method is called, all methods on this animation object fail except the <a href="/windows/desktop/api/dcompanimation/nf-dcompanimation-idcompositionanimation-reset">IDCompositionAnimation::Reset</a> method.

## -see-also

<a href="/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>