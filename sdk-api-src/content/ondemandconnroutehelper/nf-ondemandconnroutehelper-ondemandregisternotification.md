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

# OnDemandRegisterNotification function


## -description


The <b>OnDemandRegisterNotification</b> function allows an application to register to be notified when the Route Requests cache is modified. For example, this allows  the system to recycle cached connections when a Route Request is added or removed from the cache.


## -parameters




### -param callback

TBD


### -param callbackContext

TBD


### -param registrationHandle

TBD




#### - funcCallback [in]

A pointer to a function of type O<b>ONDEMAND_NOTIFICATION_CALLBACK</b> to receive the notifications.


#### - pCallbackContext [in, optional]

A pointer to a memory location containing optional context to be passed to the callback.


#### - pRegistrationHandle [out]

A pointer to a HANDLE to receive a handle to the registration in case of success.


## -returns



Returns S_OK on success.




## -remarks



The <b>ONDEMAND_NOTIFICATION_CALLBACK</b> function is defined as:

<pre class="syntax" xml:space="preserve"><code>typedef void (WINAPI *ONDEMAND_NOTIFICATION_CALLBACK) (PVOID);</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/A7FA6035-D089-4A65-8F4E-F8722C147B0F">OnDemandUnregisterNotification</a>
 

 

