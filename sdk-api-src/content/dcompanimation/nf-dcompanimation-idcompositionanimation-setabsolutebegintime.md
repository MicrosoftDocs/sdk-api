---
UID: NF:dcompanimation.IDCompositionAnimation.SetAbsoluteBeginTime
title: IDCompositionAnimation::SetAbsoluteBeginTime (dcompanimation.h)
description: Sets the absolute time at which the animation function starts.
helpviewer_keywords: ["IDCompositionAnimation interface [DirectComposition]","SetAbsoluteBeginTime method","IDCompositionAnimation.SetAbsoluteBeginTime","IDCompositionAnimation::SetAbsoluteBeginTime","SetAbsoluteBeginTime","SetAbsoluteBeginTime method [DirectComposition]","SetAbsoluteBeginTime method [DirectComposition]","IDCompositionAnimation interface","dcompanimation/IDCompositionAnimation::SetAbsoluteBeginTime","directcomp.idcompositionanimation_setabsolutebegintime"]
old-location: directcomp\idcompositionanimation_setabsolutebegintime.htm
tech.root: directcomp
ms.assetid: 661049EC-DAA2-46A5-B600-C3F0EF8B3EDF
ms.date: 12/05/2018
ms.keywords: IDCompositionAnimation interface [DirectComposition],SetAbsoluteBeginTime method, IDCompositionAnimation.SetAbsoluteBeginTime, IDCompositionAnimation::SetAbsoluteBeginTime, SetAbsoluteBeginTime, SetAbsoluteBeginTime method [DirectComposition], SetAbsoluteBeginTime method [DirectComposition],IDCompositionAnimation interface, dcompanimation/IDCompositionAnimation::SetAbsoluteBeginTime, directcomp.idcompositionanimation_setabsolutebegintime
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
 - IDCompositionAnimation::SetAbsoluteBeginTime
 - dcompanimation/IDCompositionAnimation::SetAbsoluteBeginTime
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
 - IDCompositionAnimation.SetAbsoluteBeginTime
---

# IDCompositionAnimation::SetAbsoluteBeginTime


## -description

Sets the absolute time at which the animation function starts.

## -parameters

### -param beginTime [in]

Type: <b><a href="/windows/win32/api/winnt/ns-winnt-large_integer-r1">LARGE_INTEGER</a></b>

The starting time for this animation.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

By default, an animation function starts when the first frame of the animation takes effect. For example, if an application creates a simple animation function with a single primitive at offset zero, associates the animation with some property,  and then calls the <a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice-commit">IDCompositionDevice::Commit</a> method, the first frame that includes the commit samples the animation at offset zero for the first primitive.

This implies that the actual default start time of all animations varies depending on the time between when the application creates the animation and calls <b>Commit</b>, to the time it takes the composition engine to pick up the committed changes. The application can use the <b>SetAbsoluteBeginTime</b> method to exercise finer control over the starting time of an animation.



This method does not control when animations take effect; it only affects how animations are sampled after they start. If the application specifies the exact time of the next frame as the absolute begin time, the result is the same as not calling this method at all. If the specified begin time is different from the time of the next frame, the result is one of following:



<ul>
<li>If the specified time is later than the next frame time, the animation start is delayed until the specified begin time.</li>
<li>If the specified time is earlier than the next frame time, the beginning of the animation is dropped and sampling starts into the animation function.
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>