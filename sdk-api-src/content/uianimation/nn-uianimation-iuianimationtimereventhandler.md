---
UID: NN:uianimation.IUIAnimationTimerEventHandler
title: IUIAnimationTimerEventHandler
author: windows-driver-content
description: Defines methods for handling timing events.
old-location: uianimation\iuianimationtimereventhandler.htm
old-project: UIAnimation
ms.assetid: 7d5c459e-e1f2-470b-8568-e6847acba63a
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IUIAnimationTimerEventHandler, IUIAnimationTimerEventHandler interface [Windows Animation], IUIAnimationTimerEventHandler interface [Windows Animation],described, uianimation.iuianimationtimereventhandler, uianimation/IUIAnimationTimerEventHandler
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update for Windows Vista [desktop apps | UWP apps]
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
req.typenames: UI_ANIMATION_TIMER_CLIENT_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAnimation.dll
api_name:
-	IUIAnimationTimerEventHandler
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationTimerEventHandler interface


## -description



      Defines methods for handling timing events.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationTimerEventHandler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAnimationTimerEventHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAnimationTimerEventHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3a09537a-6cf7-4824-90c6-265dafa07a1b">IUIAnimationTimerEventHandler::OnPostUpdate</a>
</td>
<td align="left" width="63%">

      Handles events that occur after an animation update is finished.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4f3dcac0-c800-48e5-82d6-b6bc3fb0409b">IUIAnimationTimerEventHandler::OnPreUpdate</a>
</td>
<td align="left" width="63%">

      Handles events that occur before an animation update begins.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/79986646-2d82-41a3-bff7-b2f0492c7a1b">IUIAnimationTimerEventHandler::OnRenderingTooSlow</a>
</td>
<td align="left" width="63%">

      Handles events that occur when the rendering frame rate 
      for an animation falls below a minimum desirable frame rate.
   

</td>
</tr>
</table> 


## -remarks




         Use 
         <a href="https://msdn.microsoft.com/ff1bae45-2199-4340-a27b-19865d2877f9">
         SetTimerEventHandler</a>
         to specify the timing events handler for an instance of
         <a href="https://msdn.microsoft.com/75d29528-005e-4f49-b8ff-651b58d58fc7">IUIAnimationTimer</a>. 
      


#### Examples

For an example, see <a href="https://msdn.microsoft.com/7abf084a-31f5-4e32-bfd1-e88fbc2bf63d">Read the Animation Variable Values and Draw Frames</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/75d29528-005e-4f49-b8ff-651b58d58fc7">
      IUIAnimationTimer</a>



<a href="https://msdn.microsoft.com/8ca8f7d8-e698-4c55-8241-5c8f7b47f0e8">
      IUIAnimationTimerClientEventHandler</a>



<a href="https://msdn.microsoft.com/f155ed12-d493-48a0-9bdf-0e1e79cbcd38">
      IUIAnimationTimerUpdateHandler
      </a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

