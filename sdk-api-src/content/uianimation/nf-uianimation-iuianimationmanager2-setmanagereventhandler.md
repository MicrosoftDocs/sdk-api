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
 

 

