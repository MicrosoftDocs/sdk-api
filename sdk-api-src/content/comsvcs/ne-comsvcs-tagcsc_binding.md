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

# tagCSC_Binding enumeration


## -description


Indicates whether all of the work that is submitted via the activity returned from <a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a> should be bound to only one single-threaded apartment (STA). This enumeration has no impact on the multithreaded apartment (MTA).


## -enum-fields




### -field CSC_NoBinding

The work submitted through the activity is not bound to a single STA.


### -field CSC_BindToPoolThread

The work submitted through the activity is bound to a single STA.


## -remarks



Binding all of the work submitted through the activity to a single STA involves a trade-off between avoiding the need to marshal interfaces to components used by many of the different bits of work versus needing to synchronize on a specific STA.

This enumeration is used only to set the thread pool binding for <a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a> when calling <a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a>. An error is returned if you try to set the thread pool binding when calling <a href="https://msdn.microsoft.com/84640b3b-1f43-4bec-abf6-c295cfb3da8b">CoEnterServiceDomain</a>. The values of this enumeration have no impact upon the MTA.




## -see-also




<a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a>



<a href="https://msdn.microsoft.com/84640b3b-1f43-4bec-abf6-c295cfb3da8b">CoEnterServiceDomain</a>



<a href="https://msdn.microsoft.com/9d2c4e6f-aa12-4874-a8e0-ca21a981b43f">IServiceThreadPoolConfig::SetBindingInfo</a>
 

 

