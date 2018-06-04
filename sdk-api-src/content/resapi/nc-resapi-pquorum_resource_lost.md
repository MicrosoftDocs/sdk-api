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

# PQUORUM_RESOURCE_LOST callback function


## -description


Called when control of the <a href="https://msdn.microsoft.com/4c2ee30e-4de2-44ba-93ba-d2d89196545e">quorum resource</a> has 
    been lost. The <b>PQUORUM_RESOURCE_LOST</b> type defines a pointer to this 
    function.


## -parameters




### -param Resource








#### - ResourceHandle [in]

Handle identifying the <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> to which this callback 
       applies. The value for <i>ResourceHandle</i> should be the handle passed in during the 
       <a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a> call for this resource.


## -returns



This function has no return values.




## -remarks



The <i>QuorumResourceLost</i> callback function is 
     called by a <a href="https://msdn.microsoft.com/e1434102-afaf-4a35-887e-a434c628bd90">resource DLL</a> to notify the 
     <a href="https://msdn.microsoft.com/caebb47f-c2c5-463e-a957-d9eefc7fc33d">Resource Monitor</a> that control of the quorum resource has 
     been lost after arbitration. A pointer to the Resource Monitor's 
     <i>QuorumResourceLost</i> callback function is passed to 
     a quorum resource DLL in the call to <a href="https://msdn.microsoft.com/dc16b785-bbb1-4917-a826-e49445a86c26">Arbitrate</a>.




## -see-also




<a href="https://msdn.microsoft.com/dc16b785-bbb1-4917-a826-e49445a86c26">Arbitrate</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a>



<a href="https://msdn.microsoft.com/6c7de7e6-a0f5-4308-8cf3-21968bd339a4">Resource DLL Callback Functions</a>
 

 

