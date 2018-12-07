---
UID: NF:uianimation.IUIAnimationManager2.EstimateNextEventTime
title: IUIAnimationManager2::EstimateNextEventTime
author: windows-sdk-content
description: Retrieves an estimate of the time interval before the next animation event.
old-location: uianimation\iuianimationmanager2_estimatenexteventtime.htm
tech.root: UIAnimation
ms.assetid: C2F049B7-287F-4EC2-A737-965E01515056
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EstimateNextEventTime, EstimateNextEventTime method [Windows Animation], EstimateNextEventTime method [Windows Animation],IUIAnimationManager2 interface, IUIAnimationManager2 interface [Windows Animation],EstimateNextEventTime method, IUIAnimationManager2.EstimateNextEventTime, IUIAnimationManager2::EstimateNextEventTime, uianimation.iuianimationmanager2_estimatenexteventtime, uianimation/IUIAnimationManager2::EstimateNextEventTime
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAnimation.h
api_name:
 - IUIAnimationManager2.EstimateNextEventTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationManager2::EstimateNextEventTime


## -description


Retrieves an estimate of  the time interval before the next animation event.


## -parameters




### -param seconds [out]

The estimated time, in seconds.


## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -see-also




<a href="https://msdn.microsoft.com/BD7DAD23-2A7D-4EE7-9BCF-8380F928674D">IUIAnimationManager2</a>



<a href="https://msdn.microsoft.com/7DDE96A5-5639-49EC-B5C0-3FBE60B84197">UI_ANIMATION_SECONDS_INFINITE
</a>
 

 

