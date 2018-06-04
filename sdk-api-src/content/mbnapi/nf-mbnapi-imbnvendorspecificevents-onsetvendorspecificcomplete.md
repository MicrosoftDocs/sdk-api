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

# IMbnVendorSpecificEvents::OnSetVendorSpecificComplete


## -description


Notification method indicating that a vendor-specific operation has completed.


## -parameters




### -param vendorOperation [in]

An <a href="https://msdn.microsoft.com/cbc905f6-c5ac-4c6a-9021-4ec00b938bb2">IMbnVendorSpecificOperation</a> interface representing the operation that completed.


### -param vendorSpecificData [in]

A byte array containing the data returned by underlying miniport driver. 


### -param requestID [in]

A request ID assigned by the Mobile Broadband service to identify the vendor-specific operation request.


## -returns



This method must return <b>S_OK</b>.




## -remarks



This byte array contains the byte by byte copy of data returned by underlying miniport driver. The Mobile Broadband service will free the memory for this field after the function call returns. If an application wants to use this data then it should copy the contents in its own memory.




## -see-also




<a href="https://msdn.microsoft.com/28507e68-5eaa-4b9d-bbb4-e276f4c213d5">IMbnVendorSpecificEvents</a>
 

 

