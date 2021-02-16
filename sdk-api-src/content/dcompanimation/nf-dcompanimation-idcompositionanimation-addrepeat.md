---
UID: NF:dcompanimation.IDCompositionAnimation.AddRepeat
title: IDCompositionAnimation::AddRepeat (dcompanimation.h)
description: Adds a repeat segment that causes the specified portion of an animation function to be repeated.
helpviewer_keywords: ["AddRepeat","AddRepeat method [DirectComposition]","AddRepeat method [DirectComposition]","IDCompositionAnimation interface","IDCompositionAnimation interface [DirectComposition]","AddRepeat method","IDCompositionAnimation.AddRepeat","IDCompositionAnimation::AddRepeat","dcompanimation/IDCompositionAnimation::AddRepeat","directcomp.idcompositionanimation_addrepeat"]
old-location: directcomp\idcompositionanimation_addrepeat.htm
tech.root: directcomp
ms.assetid: 14179e2f-3ede-4137-baa4-074bb31e1481
ms.date: 12/05/2018
ms.keywords: AddRepeat, AddRepeat method [DirectComposition], AddRepeat method [DirectComposition],IDCompositionAnimation interface, IDCompositionAnimation interface [DirectComposition],AddRepeat method, IDCompositionAnimation.AddRepeat, IDCompositionAnimation::AddRepeat, dcompanimation/IDCompositionAnimation::AddRepeat, directcomp.idcompositionanimation_addrepeat
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
 - IDCompositionAnimation::AddRepeat
 - dcompanimation/IDCompositionAnimation::AddRepeat
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
 - IDCompositionAnimation.AddRepeat
---

# IDCompositionAnimation::AddRepeat


## -description

Adds a repeat segment that causes the specified portion of an animation function to be repeated.

## -parameters

### -param beginOffset [in]

Type: <b>double</b>

The offset, in seconds, from the beginning of the animation to the point at which the repeat should begin.

### -param durationToRepeat [in]

Type: <b>double</b>

The duration, in seconds, of a portion of the animation immediately preceding the begin time that is specified by <i>beginOffset</i>.  This is the portion that will be repeated.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

This method fails if any of the parameters are NaN, positive infinity, or negative infinity.

Because animation segments must be added in increasing order, this method fails if the <i>beginOffset</i> parameter is less than or equal to the <i>beginOffset</i> parameter of the previous segment. This method also fails if this is the first segment to be added to the animation function.

This animation segment remains in effect until the begin time of the next segment. If the animation function contains no more segments, this segment remains in effect indefinitely.


#### Examples

The following example creates an animation function that includes  a repeat segment, and applies the animation to the x and y axes of a scale transform.


```cpp
HRESULT MyCreateAnimatedScaleTransform(IDCompositionDevice *pDevice, 
                                       IDCompositionVisual *pVisual)
{
    HRESULT hr = S_OK;
    IDCompositionAnimation *pAnimation = nullptr;
    IDCompositionScaleTransform *pScaleTransform = nullptr;

    // Validate the pointers.
    if (pDevice == nullptr || pVisual == nullptr)
        return E_INVALIDARG;
    
    // Create an animation object.
    hr = pDevice->CreateAnimation(&pAnimation);
    if (SUCCEEDED(hr))
    {
        // Add segments to the animation function.
        pAnimation->AddCubic(0, 1, -0.5, 0, 0);
        pAnimation->AddRepeat(3.0, 3.0);
        pAnimation->End(10, .5);

        // Create a scale transform object.
          hr = pDevice->CreateScaleTransform(&pScaleTransform);
    }

    if (SUCCEEDED(hr))
    {
        // Apply the animation to the x and y axes of the scale transform.
        pScaleTransform->SetScaleX(pAnimation);
        pScaleTransform->SetScaleY(pAnimation);

        // Apply the scale transform to the visual.
        hr = pVisual->SetTransform(pScaleTransform);
    }

    if (SUCCEEDED(hr))
    {
        // Commit the composition for rendering.
        hr = pDevice->Commit();
    }

    // Clean up.
    SafeRelease(&pAnimation);
    SafeRelease(&pScaleTransform);

    return hr;
}

```

## -see-also

<a href="/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>