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

# IUPnPDeviceFinder::StartAsyncFind


## -description


The 
<b>StartAsyncFind</b> method starts an asynchronous search operation.


## -parameters




### -param lFindData [in]

Specifies the search to start. The value of <i>lFindData</i> is the value returned by a previous call to 
<a href="https://msdn.microsoft.com/4461b53f-b630-4b4a-bc68-0cc48ef70594">IUPnPDeviceFinder::CreateAsyncFind</a>.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.




## -remarks



You can have more than one 
<b>StartAsyncFind</b> operation running at the same time; starting another 
<b>StartAsyncFind</b> does not cancel a previous 
<b>StartAsyncFind</b> operation.




## -see-also




<a href="https://msdn.microsoft.com/a4697038-8abc-42f2-9381-702fc82af90b">IUPnPDeviceFinder</a>



<a href="https://msdn.microsoft.com/d64db4fe-0b0a-430f-b198-dd49ef40b52e">IUPnPDeviceFinder::CancelAsyncFind</a>
 

 

