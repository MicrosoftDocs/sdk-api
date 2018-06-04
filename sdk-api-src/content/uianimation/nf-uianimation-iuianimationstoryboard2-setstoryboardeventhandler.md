---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IUIAnimationStoryboard2::SetStoryboardEventHandler


## -description



      Specifies a handler for storyboard events.


## -parameters




### -param handler [in, optional]


            The handler that Windows Animation should call whenever storyboard status and update events occur.
            
            The specified object must implement the
            <a href="https://msdn.microsoft.com/2AB8C0C5-2203-4778-BBEA-6D52B727FDDB">IUIAnimationStoryboardEventHandler2</a> interface or be <b>NULL</b>. See Remarks for more info.


### -param fRegisterStatusChangeForNextAnimationEvent [in]

If <b>TRUE</b>, registers the <a href="https://msdn.microsoft.com/6C428A75-755D-4171-A714-83FC65A9D972">OnStoryboardStatusChanged</a> event and includes those events in <a href="https://msdn.microsoft.com/C2F049B7-287F-4EC2-A737-965E01515056">IUIAnimationManager2::EstimateNextEventTime</a>, which estimates the time interval until the next animation event. No default value.


### -param fRegisterUpdateForNextAnimationEvent [in]

If <b>TRUE</b>, registers the <a href="https://msdn.microsoft.com/30AB185A-D555-47CA-A2E6-DAAEB0C56FCD">OnStoryboardUpdated</a> event and includes those events in <a href="https://msdn.microsoft.com/C2F049B7-287F-4EC2-A737-965E01515056">IUIAnimationManager2::EstimateNextEventTime</a>, which estimates the time interval until the next animation event. No default value.


## -returns



Returns <b>S_OK</b> if successful; otherwise an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



Passing <b>NULL</b> for the <i>handler</i> parameter causes Windows Animation to release its reference to any handler object that you passed in earlier. This technique can be essential for breaking reference cycles without having to call the <a href="https://msdn.microsoft.com/F66A987C-E020-4CD6-BE3F-440C3F8B8CF2">IUIAnimationManager2::Shutdown</a> method.




## -see-also




<a href="https://msdn.microsoft.com/507B6C2B-92C6-4AEB-82D5-3F14A332D41F">IUIAnimationStoryboard2</a>



<a href="https://msdn.microsoft.com/2AB8C0C5-2203-4778-BBEA-6D52B727FDDB">IUIAnimationStoryboardEventHandler2</a>
 

 

