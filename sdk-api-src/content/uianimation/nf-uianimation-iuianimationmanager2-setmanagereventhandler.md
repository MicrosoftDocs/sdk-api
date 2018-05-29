---
UID: NF:uianimation.IUIAnimationManager2.SetManagerEventHandler
title: IUIAnimationManager2::SetManagerEventHandler
author: windows-sdk-content
description: Specifies a handler for animation manager status updates.
old-location: uianimation\iuianimationmanager2_setmanagereventhandler.htm
old-project: UIAnimation
ms.assetid: 057CF933-4C6B-4875-82CD-27BB69ED8E4D
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IUIAnimationManager2 interface [Windows Animation],SetManagerEventHandler method, IUIAnimationManager2.SetManagerEventHandler, IUIAnimationManager2::SetManagerEventHandler, SetManagerEventHandler, SetManagerEventHandler method [Windows Animation], SetManagerEventHandler method [Windows Animation],IUIAnimationManager2 interface, uianimation.iuianimationmanager2_setmanagereventhandler, uianimation/IUIAnimationManager2::SetManagerEventHandler
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: UI_ANIMATION_TIMER_CLIENT_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAnimation.dll
api_name:
-	IUIAnimationManager2.SetManagerEventHandler
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationManager2::SetManagerEventHandler


## -description



      
         Specifies a handler for animation manager status updates.


## -parameters




### -param handler [in, optional]

The event handler to be called when the status of the animation manager changes.  
               
               The specified object must implement the
               <a href="https://msdn.microsoft.com/caefafb8-55f8-47c3-adc7-26708b90d2cd">IUIAnimationManagerEventHandler</a> interface or be <b>NULL</b>.
            See Remarks for more info.


### -param fRegisterForNextAnimationEvent [in]

If <b>TRUE</b>, specifies that <a href="https://msdn.microsoft.com/C2F049B7-287F-4EC2-A737-965E01515056">IUIAnimationManager2::EstimateNextEventTime</a> will incorporate <i>handler</i> into its estimate of the time interval until the next animation event. No default value.


## -returns



Returns <b>S_OK</b> if successful; otherwise an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



Passing <b>NULL</b> for the <i>handler</i> parameter causes Windows Animation to release its reference to any handler object that you passed in earlier. This technique can be essential for breaking reference cycles without having to call the <a href="https://msdn.microsoft.com/F66A987C-E020-4CD6-BE3F-440C3F8B8CF2">IUIAnimationManager2::Shutdown</a> method.




## -see-also




<a href="https://msdn.microsoft.com/BD7DAD23-2A7D-4EE7-9BCF-8380F928674D">IUIAnimationManager2</a>



<a href="https://msdn.microsoft.com/caefafb8-55f8-47c3-adc7-26708b90d2cd">IUIAnimationManagerEventHandler</a>
 

 

