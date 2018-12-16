---
UID: NF:uianimation.IUIAnimationStoryboard.SetStoryboardEventHandler
title: IUIAnimationStoryboard::SetStoryboardEventHandler
author: windows-sdk-content
description: Specifies a handler for storyboard events.
old-location: uianimation\iuianimationstoryboard_setstoryboardeventhandler.htm
tech.root: UIAnimation
ms.assetid: 8fbe8e94-8585-4adc-8643-3962aff6a031
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IUIAnimationStoryboard interface [Windows Animation],SetStoryboardEventHandler method, IUIAnimationStoryboard.SetStoryboardEventHandler, IUIAnimationStoryboard::SetStoryboardEventHandler, SetStoryboardEventHandler, SetStoryboardEventHandler method [Windows Animation], SetStoryboardEventHandler method [Windows Animation],IUIAnimationStoryboard interface, uianimation.iuianimationstoryboard_setstoryboardeventhandler, uianimation/IUIAnimationStoryboard::SetStoryboardEventHandler
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
 - IUIAnimationStoryboard.SetStoryboardEventHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationStoryboard::SetStoryboardEventHandler


## -description


Specifies a handler for storyboard events.


## -parameters




### -param handler [in, optional]

The handler to be called whenever storyboard status and update events occur.
            
            The specified object must implement the
            <a href="https://msdn.microsoft.com/f43f53f9-1491-4847-89ef-e65ba98a2127">IUIAnimationStoryboardEventHandler</a> interface or be <b>NULL</b>. See Remarks.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



Passing <b>NULL</b> for the <i>handler</i> parameter causes Windows Animation to release its reference to any handler object you passed in earlier. This technique can be essential for breaking reference cycles without having to call the <a href="https://msdn.microsoft.com/3bcce52c-d29a-423c-ae76-eb88cbe8c8df">IUIAnimationManager::Shutdown</a> method.




## -see-also




<a href="https://msdn.microsoft.com/6b30b660-dfa4-410f-a8de-58ea5c9a104d">IUIAnimationStoryboard</a>



<a href="https://msdn.microsoft.com/f43f53f9-1491-4847-89ef-e65ba98a2127">IUIAnimationStoryboardEventHandler</a>
 

 

