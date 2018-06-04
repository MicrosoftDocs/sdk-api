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

# IFsrmPropertyBag::AddMessage


## -description


Adds an error message to the bag.


## -parameters




### -param message [in]

The error message to add to the bag. The message is limited to 4096 characters (the message is truncated if longer than 4096 characters).


## -returns



The method returns the following return values.




## -remarks



You can add only one message to the bag. The message is written to the error log, if enabled.

If any of the following implementations returns an error code, FSRM automatically adds a message (which does not count against the one-message limit) that includes the error code and associated message string:

<ul>
<li>
<a href="https://msdn.microsoft.com/ab42430c-1e30-4576-b6f8-c0488b6230dd">IFsrmClassifierModuleImplementation::DoesPropertyValueApply</a>
</li>
<li>
<a href="https://msdn.microsoft.com/70277473-de96-40e1-980b-4eec6e7b035d">IFsrmClassifierModuleImplementation::GetPropertyValueToApply</a>
</li>
<li>
<a href="https://msdn.microsoft.com/05de6dfe-0f90-4866-bedc-72b8fea9dfac">IFsrmStorageModuleImplementation::LoadProperties</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4d31db26-9d03-46f3-a902-401f9e0d9767">IFsrmStorageModuleImplementation::SaveProperties</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/237f024d-2b1d-45d5-a63d-c530426278e6">IFsrmPropertyBag</a>



<a href="https://msdn.microsoft.com/3aa6bc28-03bb-40ea-8c56-94133c8eeb54">IFsrmPropertyBag::Messages</a>
 

 

