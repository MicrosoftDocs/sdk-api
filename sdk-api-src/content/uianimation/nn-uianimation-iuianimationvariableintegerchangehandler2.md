---
UID: NN:uianimation.IUIAnimationVariableIntegerChangeHandler2
title: IUIAnimationVariableIntegerChangeHandler2
author: windows-sdk-content
description: Defines a method for handling animation variable update events. IUIAnimationVariableIntegerChangeHandler2 handles events that occur in a specified dimension.
old-location: uianimation\iuianimationvariableintegerchangehandler2.htm
old-project: UIAnimation
ms.assetid: 778BE01B-360C-431C-9515-DE43B4F2B77D
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IUIAnimationVariableIntegerChangeHandler2, IUIAnimationVariableIntegerChangeHandler2 interface [Windows Animation], IUIAnimationVariableIntegerChangeHandler2 interface [Windows Animation],described, uianimation.iuianimationvariableintegerchangehandler2, uianimation/IUIAnimationVariableIntegerChangeHandler2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8, Windows 7 and Platform Update for Windows 7 [desktop apps | UWP apps]
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
tech.root: 
req.typenames: UI_ANIMATION_TIMER_CLIENT_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAnimation.dll
api_name:
-	IUIAnimationVariableIntegerChangeHandler2
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationVariableIntegerChangeHandler2 interface


## -description


Defines a method for handling animation variable update events. <b>IUIAnimationVariableIntegerChangeHandler2</b> handles events that occur in a specified dimension.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationVariableIntegerChangeHandler2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAnimationVariableIntegerChangeHandler2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAnimationVariableIntegerChangeHandler2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76889784-BF1B-475B-8D84-201BEE6F0594">OnIntegerValueChanged</a>
</td>
<td align="left" width="63%">

         Handles events that occur when the integer value of an animation variable changes in the specified dimension.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/C878B86A-87AD-457A-802A-9A329B401B08">
         IUIAnimationVariable2::GetIntegerValue</a>



<a href="https://msdn.microsoft.com/4327AC4A-2C2C-4C1A-AFCD-D2BA8ECEBA12">IUIAnimationVariable2::SetVariableIntegerChangeHandler</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

