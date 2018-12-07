---
UID: NF:uianimation.IUIAnimationManager2.Shutdown
title: IUIAnimationManager2::Shutdown
author: windows-sdk-content
description: Shuts down the animation manager and all its associated objects.
old-location: uianimation\iuianimationmanager2_shutdown.htm
tech.root: UIAnimation
ms.assetid: F66A987C-E020-4CD6-BE3F-440C3F8B8CF2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IUIAnimationManager2 interface [Windows Animation],Shutdown method, IUIAnimationManager2.Shutdown, IUIAnimationManager2::Shutdown, Shutdown, Shutdown method [Windows Animation], Shutdown method [Windows Animation],IUIAnimationManager2 interface, uianimation.iuianimationmanager2_shutdown, uianimation/IUIAnimationManager2::Shutdown
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8, Windows 7 and Platform Update for Windows 7 [desktop apps \| UWP apps]
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
 - IUIAnimationManager2.Shutdown
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationManager2::Shutdown


## -description


Shuts down the animation manager and all its associated objects.


## -parameters






## -returns



Returns S_OK if successful; otherwise an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



Calling this method directs the animation manager, and all the objects it created, to 
         release all their pointers to other objects. After <b>IUIAnimationManager2::Shutdown</b> has been called, no other methods may be called on the animation manager or on any objects that it created. An application can call this method to clean up if there is any possibility that the application has introduced a reference cycle that includes some animation objects.




## -see-also




<a href="https://msdn.microsoft.com/BD7DAD23-2A7D-4EE7-9BCF-8380F928674D">IUIAnimationManager2</a>
 

 

