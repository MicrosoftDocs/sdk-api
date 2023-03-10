---
UID: NF:dcompanimation.IDCompositionAnimation.Reset
title: IDCompositionAnimation::Reset (dcompanimation.h)
description: Resets the animation function so that it contains no segments.
helpviewer_keywords: ["IDCompositionAnimation interface [DirectComposition]","Reset method","IDCompositionAnimation.Reset","IDCompositionAnimation::Reset","Reset","Reset method [DirectComposition]","Reset method [DirectComposition]","IDCompositionAnimation interface","dcompanimation/IDCompositionAnimation::Reset","directcomp.idcompositionanimation_reset"]
old-location: directcomp\idcompositionanimation_reset.htm
tech.root: directcomp
ms.assetid: 3745fff0-eefa-4262-9ce3-9ab812264c1d
ms.date: 12/05/2018
ms.keywords: IDCompositionAnimation interface [DirectComposition],Reset method, IDCompositionAnimation.Reset, IDCompositionAnimation::Reset, Reset, Reset method [DirectComposition], Reset method [DirectComposition],IDCompositionAnimation interface, dcompanimation/IDCompositionAnimation::Reset, directcomp.idcompositionanimation_reset
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
 - IDCompositionAnimation::Reset
 - dcompanimation/IDCompositionAnimation::Reset
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
 - IDCompositionAnimation.Reset
---

# IDCompositionAnimation::Reset


## -description

Resets the animation function so that it contains no segments.



## -returns

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

This method returns the animation function to a clean state, as when the animation was first constructed. After this method is called, the next segment to be added becomes the first segment of the animation function. Because it is the first segment, it can have any non-negative beginning offset.

## -see-also

<a href="/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>
