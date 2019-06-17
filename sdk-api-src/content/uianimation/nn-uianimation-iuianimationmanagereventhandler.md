---
UID: NN:uianimation.IUIAnimationManagerEventHandler
title: IUIAnimationManagerEventHandler (uianimation.h)
author: windows-sdk-content
description: Defines a method for handling status updates to an animation manager.
old-location: uianimation\iuianimationmanagereventhandler.htm
tech.root: UIAnimation
ms.assetid: caefafb8-55f8-47c3-adc7-26708b90d2cd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIAnimationManagerEventHandler, IUIAnimationManagerEventHandler interface [Windows Animation], IUIAnimationManagerEventHandler interface [Windows Animation],described, uianimation.iuianimationmanagereventhandler, uianimation/IUIAnimationManagerEventHandler
ms.topic: interface
f1_keywords: ["uianimation/IUIAnimationManagerEventHandler"]
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
 - IUIAnimationManagerEventHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAnimationManagerEventHandler interface


## -description


Defines a method for handling status updates to an animation manager.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationManagerEventHandler</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAnimationManagerEventHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAnimationManagerEventHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanagereventhandler-onmanagerstatuschanged">OnManagerStatusChanged</a>
</td>
<td align="left" width="63%">
Handles status changes to the animation manager.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-getstatus">IUIAnimationManager::GetStatus</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/ne-uianimation-__midl___midl_itf_uianimation_0000_0000_0002">UI_ANIMATION_MANAGER_STATUS</a>
 

 

