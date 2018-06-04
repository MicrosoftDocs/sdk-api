---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

