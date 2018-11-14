---
UID: NF:uianimation.IUIAnimationStoryboard.Schedule
title: IUIAnimationStoryboard::Schedule
author: windows-sdk-content
description: Directs the storyboard to schedule itself for play.
old-location: uianimation\iuianimationstoryboard_schedule.htm
tech.root: UIAnimation
ms.assetid: b47d4ffd-ae51-40e7-8f91-9d7b7b2901c8
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IUIAnimationStoryboard interface [Windows Animation],Schedule method, IUIAnimationStoryboard.Schedule, IUIAnimationStoryboard::Schedule, Schedule, Schedule method [Windows Animation], Schedule method [Windows Animation],IUIAnimationStoryboard interface, uianimation.iuianimationstoryboard_schedule, uianimation/IUIAnimationStoryboard::Schedule
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAnimation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAnimation.dll
api_name:
 - IUIAnimationStoryboard.Schedule
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- uianimation.h
: 
- IUIAnimationStoryboard.Schedule
: 
---

# IUIAnimationStoryboard::Schedule


## -description


Directs the storyboard to schedule itself for play.


## -parameters




### -param timeNow [in]

The current time.


### -param schedulingResult [out, optional]

The result of the scheduling request.
            This parameter can be omitted from calls to this method.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



This method directs a storyboard to attempt to add itself to the schedule of playing storyboards. The rules are as follows:

<ul>
<li>
If there are no playing storyboards animating any of the same animation variables, the attempt succeeds and the storyboard starts playing immediately.

</li>
<li>
If the storyboard has priority to cancel, trim, conclude, or compress conflicting storyboards, the attempt to schedule succeeds and the storyboard begins playing as soon as possible.

</li>
<li>
If the storyboard does not have priority, the attempt fails and the <i>schedulingResult</i> parameter is set to <b>UI_ANIMATION_SCHEDULING_INSUFFICIENT_PRIORITY</b>.

</li>
</ul>
If this method is called from a handler for <a href="https://msdn.microsoft.com/e1ccf0e3-64fc-444e-a27b-1a5bc1d9d6fd">OnStoryboardStatusChanged</a> events, the <i>schedulingResult</i> parameter is set to <b>UI_ANIMATION_SCHEDULING_DEFERRED</b>.  The only way to determine whether the storyboard is successfully scheduled is to set a storyboard event handler and check whether the storyboard's status ever becomes <b>UI_ANIMATION_STORYBOARD_INSUFFICIENT_PRIORITY</b>.

It is possible reuse a storyboard by calling <b>Schedule</b> again after its status has reached <b>UI_ANIMATION_STORYBOARD_READY</b>.  An attempt to schedule a storyboard when it is in any state other than <b>UI_ANIMATION_STORYBOARD_BUILDING</b> or <b>UI_ANIMATION_STORYBOARD_READY</b> fails, and  <i>schedulingResult</i> is set to <b>UI_ANIMATION_SCHEDULING_ALREADY_SCHEDULED</b>.


#### Examples

The following example gets the current time and schedules the storyboard. For an additional example, see <a href="https://msdn.microsoft.com/f3c8fe34-8bca-4421-a390-9e0ba9af27b4">Schedule a Storyboard</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Get the current time and schedule the storyboard
UI_ANIMATION_SECONDS secondsNow;
hr = m_pAnimationTimer-&gt;GetTime(
    &amp;secondsNow
    );
if (SUCCEEDED(hr))
{
    UI_ANIMATION_SCHEDULING_RESULT schedulingResult;
    hr = pStoryboard-&gt;Schedule(
        secondsNow,
        &amp;schedulingResult
        );
    if (SUCCEEDED(hr))
    {
        if (schedulingResult == UI_ANIMATION_SCHEDULING_SUCCEEDED)
        {
            ...
        }
        else
        {
            ...
        }
    }
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/6b30b660-dfa4-410f-a8de-58ea5c9a104d">IUIAnimationStoryboard</a>



<a href="https://msdn.microsoft.com/2350dbd0-3a67-4832-94dd-56adce80a387">IUIAnimationStoryboard::Abandon</a>



<a href="https://msdn.microsoft.com/82f915df-c031-41e9-8347-044b37793182">IUIAnimationStoryboard::Conclude</a>



<a href="https://msdn.microsoft.com/45d0872a-dbcf-4151-a880-80b2c6fb884c">IUIAnimationStoryboard::Finish</a>



<a href="https://msdn.microsoft.com/8ee9a17f-c57c-49df-950d-491e05ba8768">IUIAnimationStoryboard::GetStatus</a>



<a href="https://msdn.microsoft.com/32654e4b-158b-4d1a-afc7-98f90212b33b">IUIAnimationTimer::GetTime</a>



<a href="https://msdn.microsoft.com/2d62589a-9121-4af6-b704-566a28dcc21e">UI_ANIMATION_SCHEDULING_RESULT</a>



<a href="https://msdn.microsoft.com/02830092-0070-44dc-8db2-239941134473">UI_ANIMATION_STORYBOARD_STATUS</a>
 

 

