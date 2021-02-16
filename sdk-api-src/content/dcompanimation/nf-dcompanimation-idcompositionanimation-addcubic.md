---
UID: NF:dcompanimation.IDCompositionAnimation.AddCubic
title: IDCompositionAnimation::AddCubic (dcompanimation.h)
description: Adds a cubic polynomial segment to the animation function.
helpviewer_keywords: ["AddCubic","AddCubic method [DirectComposition]","AddCubic method [DirectComposition]","IDCompositionAnimation interface","IDCompositionAnimation interface [DirectComposition]","AddCubic method","IDCompositionAnimation.AddCubic","IDCompositionAnimation::AddCubic","dcompanimation/IDCompositionAnimation::AddCubic","directcomp.idcompositionanimation_addcubic"]
old-location: directcomp\idcompositionanimation_addcubic.htm
tech.root: directcomp
ms.assetid: d80ab2db-0d88-46ed-a40d-4408bf315a85
ms.date: 12/05/2018
ms.keywords: AddCubic, AddCubic method [DirectComposition], AddCubic method [DirectComposition],IDCompositionAnimation interface, IDCompositionAnimation interface [DirectComposition],AddCubic method, IDCompositionAnimation.AddCubic, IDCompositionAnimation::AddCubic, dcompanimation/IDCompositionAnimation::AddCubic, directcomp.idcompositionanimation_addcubic
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
 - IDCompositionAnimation::AddCubic
 - dcompanimation/IDCompositionAnimation::AddCubic
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
 - IDCompositionAnimation.AddCubic
---

# IDCompositionAnimation::AddCubic


## -description

Adds a cubic polynomial segment to the animation function.

## -parameters

### -param beginOffset [in]

Type: <b>double</b>

The offset, in seconds, from the beginning of the animation function to the point when this segment should take effect.

### -param constantCoefficient [in]

Type: <b>float</b>

The constant coefficient of the polynomial.

### -param linearCoefficient [in]

Type: <b>float</b>

The linear coefficient of the polynomial.

### -param quadraticCoefficient [in]

Type: <b>float</b>

The quadratic coefficient of the polynomial.

### -param cubicCoefficient [in]

Type: <b>float</b>

The cubic coefficient of the polynomial.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

A cubic segment transitions time along a cubic polynomial.  For a given time input (t), the output value is given by the following equation.



<i>x</i>(<i>t</i>) = <i>at</i>³ + <i>bt</i>² + <i>ct</i> + <i>d</i>

This method fails if any of the parameters are NaN, positive infinity, or negative infinity.

Because animation segments must be added in increasing order, this method fails if the <i>beginOffset</i> parameter is less than or equal to the <i>beginOffset</i> parameter of the previous segment, if any.

This animation segment remains in effect until the begin time of the next segment in the animation function. If the animation function contains no more segments, this segment remains in effect indefinitely. 

If all coefficients except <i>constantCoefficient</i>  are zero, the value of this segment remains constant over time, and the animation does not cause a recomposition for the duration of the segment.


#### Examples

The following example creates an animation function with two cubic polynomial segments.


```cpp
HRESULT DoAnimatedRotation(IDCompositionDevice *pDevice,
                           IDCompositionRotateTransform *pRotateTransform,
                           IDCompositionVisual *pVisual, 
                           float animationTime) 
{
    HRESULT hr = S_OK;
    IDCompositionAnimation *pAnimation = nullptr;

    // Create an animation object. 
    hr = pDevice->CreateAnimation(&pAnimation);

    if (SUCCEEDED(hr)) 
    {
        // Create the animation function by adding cubic polynomial segments.
        // For a given time input (t), the output value is
        // a*t^3 + b* t^2 + c*t + d.
        // 
        // The following segment will rotate the visual clockwise.
        pAnimation->AddCubic(
            0.0,                                // Begin offset
            0.0,                                // Constant coefficient - d
            (360.0f * 1.0f) / animationTime,    // Linear coefficient - c
            0.0,                                // Quadratic coefficient - b
            0.0);                               // Cubic coefficient - a

        // The following segment will rotate the visual counterclockwise.
        pAnimation->AddCubic(
            animationTime,
            0.0,
            -(360.0f * 1.0f) / animationTime,
            0.0,
            0.0);

        // Set the end of the animation.
        pAnimation->End(
            2 * animationTime,  // End offset
            0.0);               // End value

        // Apply the animation to the Angle property of the
        // rotate transform. 
        hr = pRotateTransform->SetAngle(pAnimation);
    }

    if (SUCCEEDED(hr))
    {
        // Apply the rotate transform object to a visual.
        hr = pVisual->SetTransform(pRotateTransform);
    }

    if (SUCCEEDED(hr))
    {
        // Commit the changes to the composition.
        hr = pDevice->Commit();
    }

    SafeRelease(&pAnimation);

    return hr;
}

```

## -see-also

<a href="/windows/desktop/directcomp/animation">Animation</a>



<a href="/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>