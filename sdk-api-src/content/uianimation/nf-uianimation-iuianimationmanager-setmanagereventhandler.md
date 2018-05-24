---
UID: NF:uianimation.IUIAnimationManager.SetManagerEventHandler
title: IUIAnimationManager::SetManagerEventHandler
author: windows-driver-content
description: Specifies a handler for animation manager status updates.
old-location: uianimation\iuianimationmanager_setmanagereventhandler.htm
old-project: UIAnimation
ms.assetid: 89c4df40-6faa-4b7c-a255-289d1f8a6254
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IUIAnimationManager interface [Windows Animation],SetManagerEventHandler method, IUIAnimationManager.SetManagerEventHandler, IUIAnimationManager::SetManagerEventHandler, SetManagerEventHandler, SetManagerEventHandler method [Windows Animation], SetManagerEventHandler method [Windows Animation],IUIAnimationManager interface, uianimation.iuianimationmanager_setmanagereventhandler, uianimation/IUIAnimationManager::SetManagerEventHandler
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
-	IUIAnimationManager.SetManagerEventHandler
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationManager::SetManagerEventHandler


## -description



      
         Specifies a handler for animation manager status updates.


## -parameters




### -param handler [in, optional]

The event handler to be called when the status of the animation manager changes.  
               
               The specified object must implement the
               <a href="https://msdn.microsoft.com/caefafb8-55f8-47c3-adc7-26708b90d2cd">IUIAnimationManagerEventHandler</a> interface or be <b>NULL</b>.
            See Remarks section for more information.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



Passing <b>NULL</b> for the <i>handler</i> parameter causes Windows Animation to release its reference to any handler object that you passed in earlier. This technique can be essential for breaking reference cycles without having to call the <a href="https://msdn.microsoft.com/3bcce52c-d29a-423c-ae76-eb88cbe8c8df">IUIAnimationManager::Shutdown</a> method.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/c4f746c3-e47c-4b82-a41b-e2c0d177d097">Update the Animation Manager and Draw Frames</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/21f16c65-90aa-4b1f-93bc-8ee0488c6ded">IUIAnimationManager</a>



<a href="https://msdn.microsoft.com/caefafb8-55f8-47c3-adc7-26708b90d2cd">IUIAnimationManagerEventHandler</a>
 

 

