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

# IUIAnimationTransition::GetDuration


## -description



   
   Gets the duration of the transition.


## -parameters




### -param duration [out]

The duration of the transition, in seconds.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UI_E_VALUE_NOT_DETERMINED</b></dt>
</dl>
</td>
<td width="60%">
The requested value for the duration cannot be determined.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UI_E_STORYBOARD_ACTIVE</b></dt>
</dl>
</td>
<td width="60%">
The storyboard for this transition is currently in the schedule.

</td>
</tr>
</table>
 




## -remarks



An application should typically call the <a href="https://msdn.microsoft.com/5cb22573-a318-4682-bc82-0a81c9dbdcbe">IUIAnimationTransition::IsDurationKnown</a> method before calling this method. This method should not be called when the storyboard to which the transition has been added is scheduled or playing.


#### Examples

The following shows how to get the duration of a transition.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>hr = pTransition-&gt;IsDurationKnown();
if (SUCCEEDED(hr))
{
    bool fDurationKnown = (hr == S_OK); 
    if (fDurationKnown)
    {
        UI_ANIMATION_SECONDS duration;
        hr = pTransition-&gt;GetDuration(&amp;duration);
        if (SUCCEEDED(hr))
        {        
            ...
        }
    }
    else
    {
        ...
    }
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/99804a2f-82c9-494c-b75d-69e66f1e49ef">IUIAnimationTransition</a>



<a href="https://msdn.microsoft.com/5cb22573-a318-4682-bc82-0a81c9dbdcbe">IUIAnimationTransition::IsDurationKnown</a>
 

 

