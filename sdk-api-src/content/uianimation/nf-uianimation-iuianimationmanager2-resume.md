---
UID: NF:uianimation.IUIAnimationManager2.Resume
title: IUIAnimationManager2::Resume (uianimation.h)
author: windows-sdk-content
description: Resumes all animations.
old-location: uianimation\iuianimationmanager2_resume.htm
tech.root: UIAnimation
ms.assetid: 943BCFBB-3E16-4CC8-BA9F-06D4C99B1DF0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIAnimationManager2 interface [Windows Animation],Resume method, IUIAnimationManager2.Resume, IUIAnimationManager2::Resume, Resume, Resume method [Windows Animation], Resume method [Windows Animation],IUIAnimationManager2 interface, uianimation.iuianimationmanager2_resume, uianimation/IUIAnimationManager2::Resume
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
 - IUIAnimationManager2.Resume
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAnimationManager2::Resume


## -description


Resumes all animations.


## -parameters






## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



When an animation manager is resumed, and at least one animation is currently scheduled or playing, its status is set to <a href="https://msdn.microsoft.com/en-us/library/Dd317043(v=VS.85).aspx">UI_ANIMATION_MANAGER_BUSY</a>.




## -see-also




<a href="https://msdn.microsoft.com/BD7DAD23-2A7D-4EE7-9BCF-8380F928674D">IUIAnimationManager2</a>



<a href="https://msdn.microsoft.com/838140c3-12ca-4909-a0f8-713b5472e5a9">IUIAnimationManager::GetStatus</a>



<a href="https://msdn.microsoft.com/52b11e79-9930-4fd8-84b4-152917090519">IUIAnimationManager::Pause</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd317043(v=VS.85).aspx">UI_ANIMATION_MANAGER_STATUS</a>
 

 

