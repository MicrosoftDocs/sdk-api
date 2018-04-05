---
UID: NF:dcompanimation.IDCompositionAnimation.SetAbsoluteBeginTime
title: IDCompositionAnimation::SetAbsoluteBeginTime method
author: windows-driver-content
description: Sets the absolute time at which the animation function starts.
old-location: directcomp\idcompositionanimation_setabsolutebegintime.htm
old-project: directcomp
ms.assetid: 661049EC-DAA2-46A5-B600-C3F0EF8B3EDF
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IDCompositionAnimation, IDCompositionAnimation interface [DirectComposition], SetAbsoluteBeginTime method, IDCompositionAnimation::SetAbsoluteBeginTime, SetAbsoluteBeginTime method [DirectComposition], SetAbsoluteBeginTime method [DirectComposition], IDCompositionAnimation interface, SetAbsoluteBeginTime,IDCompositionAnimation.SetAbsoluteBeginTime, dcompanimation/IDCompositionAnimation::SetAbsoluteBeginTime, directcomp.idcompositionanimation_setabsolutebegintime
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
req.typenames: DEV_BROADCAST_VOLUME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Dcomp.dll
api_name:
-	IDCompositionAnimation.SetAbsoluteBeginTime
product: Windows
targetos: Windows
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
---

# IDCompositionAnimation::SetAbsoluteBeginTime method


## -description


Sets the absolute time at which the animation function starts.


## -parameters




### -param beginTime [in]

Type: <b><a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a></b>

The starting time for this animation.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



By default, an animation function starts when the first frame of the animation takes effect. For example, if an application creates a simple animation function with a single primitive at offset zero, associates the animation with some property,  and then calls the <a href="https://msdn.microsoft.com/49a6d33d-7454-44be-b8ca-602b247d4eab">IDCompositionDevice::Commit</a> method, the first frame that includes the commit samples the animation at offset zero for the first primitive.

This implies that the actual default start time of all animations varies depending on the time between when the application creates the animation and calls <b>Commit</b>, to the time it takes the composition engine to pick up the committed changes. The application can use the <b>SetAbsoluteBeginTime</b> method to exercise finer control over the starting time of an animation.



This method does not control when animations take effect; it only affects how animations are sampled after they start. If the application specifies the exact time of the next frame as the absolute begin time, the result is the same as not calling this method at all. If the specified begin time is different from the time of the next frame, the result is one of following:



<ul>
<li>If the specified time is later than the next frame time, the animation start is delayed until the specified begin time.</li>
<li>If the specified time is earlier than the next frame time, the beginning of the animation is dropped and sampling starts into the animation function.
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/f914e14b-4ac0-4591-9b7f-6b45b88baaaa">IDCompositionAnimation</a>
 

 

