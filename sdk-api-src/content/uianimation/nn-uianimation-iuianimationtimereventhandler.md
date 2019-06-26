---
UID: NN:uianimation.IUIAnimationTimerEventHandler
title: IUIAnimationTimerEventHandler (uianimation.h)
author: windows-sdk-content
description: Defines methods for handling timing events.
old-location: uianimation\iuianimationtimereventhandler.htm
tech.root: UIAnimation
ms.assetid: 7d5c459e-e1f2-470b-8568-e6847acba63a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIAnimationTimerEventHandler, IUIAnimationTimerEventHandler interface [Windows Animation], IUIAnimationTimerEventHandler interface [Windows Animation],described, uianimation.iuianimationtimereventhandler, uianimation/IUIAnimationTimerEventHandler
ms.topic: interface
f1_keywords: 
 - "uianimation/IUIAnimationTimerEventHandler"
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
 - IUIAnimationTimerEventHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAnimationTimerEventHandler interface


## -description


Defines methods for handling timing events.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationTimerEventHandler</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAnimationTimerEventHandler</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimereventhandler-onpostupdate">IUIAnimationTimerEventHandler::OnPostUpdate</a>
</td>
<td align="left" width="63%">
Handles events that occur after an animation update is finished.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimereventhandler-onpreupdate">IUIAnimationTimerEventHandler::OnPreUpdate</a>
</td>
<td align="left" width="63%">
Handles events that occur before an animation update begins.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimereventhandler-onrenderingtooslow">IUIAnimationTimerEventHandler::OnRenderingTooSlow</a>
</td>
<td align="left" width="63%">
Handles events that occur when the rendering frame rate 
      for an animation falls below a minimum desirable frame rate.
   

</td>
</tr>
</table> 


## -remarks



Use 
         <a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimer-settimereventhandler">SetTimerEventHandler</a>to specify the timing events handler for an instance of
         <a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimer">IUIAnimationTimer</a>. 
      


#### Examples

For an example, see <a href="https://docs.microsoft.com/windows/desktop/UIAnimation/updating---application-driven-animation">Read the Animation Variable Values and Draw Frames</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimer">IUIAnimationTimer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimerclienteventhandler">IUIAnimationTimerClientEventHandler</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimerupdatehandler">IUIAnimationTimerUpdateHandler
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

