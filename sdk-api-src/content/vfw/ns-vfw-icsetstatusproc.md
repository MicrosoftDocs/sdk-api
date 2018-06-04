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

# ICSETSTATUSPROC structure


## -description



The <b>ICSETSTATUSPROC</b> structure contains status information used with the <a href="https://msdn.microsoft.com/a1bcd840-b94b-487e-91d6-67411a8a3a2d">ICM_SET_STATUS_PROC</a> message.




## -struct-fields




### -field dwFlags

Reserved; set to zero.


### -field lParam

Parameter that contains a constant to pass to the status procedure.


### -field Status

 




#### - fpfnStatus

Pointer to the status function. Specify <b>NULL</b> if status messages should not be sent. For more information about the callback function, see the <a href="https://msdn.microsoft.com/a24b8a05-71f3-488b-a521-5c43955c5ed2">MyStatusProc</a> function.


## -see-also




<a href="https://msdn.microsoft.com/a1bcd840-b94b-487e-91d6-67411a8a3a2d">ICM_SET_STATUS_PROC</a>



<a href="https://msdn.microsoft.com/a24b8a05-71f3-488b-a521-5c43955c5ed2">MyStatusProc</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>



<a href="https://msdn.microsoft.com/129a65a7-cac3-47e0-9e9c-6e5a4a260c73">Video Compression Structures</a>
 

 

