---
UID: NF:dcompanimation.IDCompositionAnimation.AddRepeat
title: IDCompositionAnimation::AddRepeat
author: windows-sdk-content
description: Adds a repeat segment that causes the specified portion of an animation function to be repeated.
old-location: directcomp\idcompositionanimation_addrepeat.htm
tech.root: directcomp
ms.assetid: 14179e2f-3ede-4137-baa4-074bb31e1481
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: AddRepeat, AddRepeat method [DirectComposition], AddRepeat method [DirectComposition],IDCompositionAnimation interface, IDCompositionAnimation interface [DirectComposition],AddRepeat method, IDCompositionAnimation.AddRepeat, IDCompositionAnimation::AddRepeat, dcompanimation/IDCompositionAnimation::AddRepeat, directcomp.idcompositionanimation_addrepeat
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionAnimation.AddRepeat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method fails if any of the parameters are NaN, positive infinity, or negative infinity.

Because animation segments must be added in increasing order, this method fails if the <i>beginOffset</i> parameter is less than or equal to the <i>beginOffset</i> parameter of the previous segment. This method also fails if this is the first segment to be added to the animation function.

This animation segment remains in effect until the begin time of the next segment. If the animation function contains no more segments, this segment remains in effect indefinitely.


#### Examples

The following example creates an animation function that includes  a repeat segment, and applies the animation to the x and y axes of a scale transform.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT MyCreateAnimatedScaleTransform(IDCompositionDevice *pDevice, 
                                       IDCompositionVisual *pVisual)
{
    HRESULT hr = S_OK;
    IDCompositionAnimation *pAnimation = nullptr;
    IDCompositionScaleTransform *pScaleTransform = nullptr;

    // Validate the pointers.
    if (pDevice == nullptr || pVisual == nullptr)
        return E_INVALIDARG;
    
    // Create an animation object.
    hr = pDevice-&gt;CreateAnimation(&amp;pAnimation);
    if (SUCCEEDED(hr))
    {
        // Add segments to the animation function.
        pAnimation-&gt;AddCubic(0, 1, -0.5, 0, 0);
        pAnimation-&gt;AddRepeat(3.0, 3.0);
        pAnimation-&gt;End(10, .5);

        // Create a scale transform object.
          hr = pDevice-&gt;CreateScaleTransform(&amp;pScaleTransform);
    }

    if (SUCCEEDED(hr))
    {
        // Apply the animation to the x and y axes of the scale transform.
        pScaleTransform-&gt;SetScaleX(pAnimation);
        pScaleTransform-&gt;SetScaleY(pAnimation);

        // Apply the scale transform to the visual.
        hr = pVisual-&gt;SetTransform(pScaleTransform);
    }

    if (SUCCEEDED(hr))
    {
        // Commit the composition for rendering.
        hr = pDevice-&gt;Commit();
    }

    // Clean up.
    SafeRelease(&amp;pAnimation);
    SafeRelease(&amp;pScaleTransform);

    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f914e14b-4ac0-4591-9b7f-6b45b88baaaa">IDCompositionAnimation</a>
 

 

