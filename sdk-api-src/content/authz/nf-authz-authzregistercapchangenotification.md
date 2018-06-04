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

# AuthzRegisterCapChangeNotification function


## -description


The <b>AuthzRegisterCapChangeNotification</b> function registers a CAP update notification callback.


## -parameters




### -param phCapChangeSubscription [out]

Pointer to the CAP change notification subscription handle. When you have finished using the handle, unsubscribe by passing this parameter to the <a href="https://msdn.microsoft.com/79374C66-CD50-4351-A16B-AF79A579AF74">AuthzUnregisterCapChangeNotification</a> function.


### -param pfnCapChangeCallback [in]

The CAP change notification callback function.


### -param pCallbackContext [in, optional]

The context of the user to be passed to the callback function.


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function is intended for applications that manually manage CAP usage to get notified of CAP changes in the system. 




## -see-also




<a href="https://msdn.microsoft.com/79374C66-CD50-4351-A16B-AF79A579AF74">AuthzUnregisterCapChangeNotification</a>



<a href="https://msdn.microsoft.com/E3E43D9F-6826-468A-86E9-AC8F9A381FD4">Central Access Policies</a>



<a href="https://msdn.microsoft.com/dc98b23e-ce42-4d4a-a285-c0b7b5e2a478">How AccessCheck Works</a>
 

 

