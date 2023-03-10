---
UID: NF:dcompanimation.IDCompositionAnimation.AddSinusoidal
title: IDCompositionAnimation::AddSinusoidal (dcompanimation.h)
description: Adds a sinusoidal segment to the animation function.
helpviewer_keywords: ["AddSinusoidal","AddSinusoidal method [DirectComposition]","AddSinusoidal method [DirectComposition]","IDCompositionAnimation interface","IDCompositionAnimation interface [DirectComposition]","AddSinusoidal method","IDCompositionAnimation.AddSinusoidal","IDCompositionAnimation::AddSinusoidal","dcompanimation/IDCompositionAnimation::AddSinusoidal","directcomp.idcompositionanimation_addsinusoidal"]
old-location: directcomp\idcompositionanimation_addsinusoidal.htm
tech.root: directcomp
ms.assetid: C54768ED-30A7-45E8-8CE0-33F06E48EA10
ms.date: 12/05/2018
ms.keywords: AddSinusoidal, AddSinusoidal method [DirectComposition], AddSinusoidal method [DirectComposition],IDCompositionAnimation interface, IDCompositionAnimation interface [DirectComposition],AddSinusoidal method, IDCompositionAnimation.AddSinusoidal, IDCompositionAnimation::AddSinusoidal, dcompanimation/IDCompositionAnimation::AddSinusoidal, directcomp.idcompositionanimation_addsinusoidal
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
 - IDCompositionAnimation::AddSinusoidal
 - dcompanimation/IDCompositionAnimation::AddSinusoidal
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
 - IDCompositionAnimation.AddSinusoidal
---

# IDCompositionAnimation::AddSinusoidal


## -description

Adds a sinusoidal segment to the animation function.

## -parameters

### -param beginOffset

Type: <b>double</b>

The offset, in seconds, from the beginning of the animation function to the point when this segment should take effect.

### -param bias

Type: <b>float</b>

A constant that is added to the sinusoidal.

### -param amplitude

Type: <b>float</b>

A scale factor that is applied to the sinusoidal.

### -param frequency

Type: <b>float</b>

A scale factor that is applied to the time offset, in Hertz.

### -param phase

Type: <b>float</b>

A constant that is added to the time offset, in degrees.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

This method fails if any of the parameters are NaN, positive infinity, or negative infinity, or if the <i>beginOffset</i> parameter is negative.



Because animation segments must be added in increasing order, this method fails if the <i>beginOffset</i> parameter is less than or equal to the <i>beginOffset</i> parameter of the previous segment, if any.

This animation segment remains in effect until the begin time of the next segment in the animation function. If the animation function contains no more segments, this segment remains in effect indefinitely.

## -see-also

<a href="/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>