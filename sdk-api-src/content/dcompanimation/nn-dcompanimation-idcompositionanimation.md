---
UID: NN:dcompanimation.IDCompositionAnimation
title: IDCompositionAnimation
author: windows-sdk-content
description: Represents a function for animating one or more properties of one or more Microsoft DirectComposition objects.
old-location: directcomp\idcompositionanimation.htm
tech.root: directcomp
ms.assetid: f914e14b-4ac0-4591-9b7f-6b45b88baaaa
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IDCompositionAnimation, IDCompositionAnimation interface [DirectComposition], IDCompositionAnimation interface [DirectComposition],described, dcompanimation/IDCompositionAnimation, directcomp.idcompositionanimation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IDCompositionAnimation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionAnimation interface


## -description


Represents a function for animating one or more  properties of one or more  Microsoft DirectComposition objects. Any object property that takes a scalar value can be animated.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionAnimation</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDCompositionAnimation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDCompositionAnimation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d80ab2db-0d88-46ed-a40d-4408bf315a85">AddCubic</a>
</td>
<td align="left" width="63%">
Adds a cubic polynomial segment to the animation function.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14179e2f-3ede-4137-baa4-074bb31e1481">AddRepeat</a>
</td>
<td align="left" width="63%">
Adds a repeat segment that causes the specified portion of an animation function to be repeated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C54768ED-30A7-45E8-8CE0-33F06E48EA10">AddSinusoidal</a>
</td>
<td align="left" width="63%">
Adds a sinusoidal segment to the animation function.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71287ae2-d930-4e96-8c12-538d2b58ccc6">End</a>
</td>
<td align="left" width="63%">
Adds an end segment that marks the end of an animation function.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3745fff0-eefa-4262-9ce3-9ab812264c1d">Reset</a>
</td>
<td align="left" width="63%">
Resets the animation function so that it contains no segments.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/661049EC-DAA2-46A5-B600-C3F0EF8B3EDF">SetAbsoluteBeginTime</a>
</td>
<td align="left" width="63%">
Sets the absolute time at which the animation function starts.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/e32193b2-de93-417e-9fe0-49f8e45f7a01">IDCompositionDevice::CreateAnimation</a>
 

 

