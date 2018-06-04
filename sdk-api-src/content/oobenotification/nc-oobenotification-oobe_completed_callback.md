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

# OOBE_COMPLETED_CALLBACK callback function


## -description


Application-defined callback function used with the <a href="https://msdn.microsoft.com/D1581B09-06A7-483F-929D-1AF93832942D">RegisterWaitUntilOOBECompleted</a> function.


## -parameters




### -param CallbackContext

Pointer to the callback context. This is the value passed to the <a href="https://msdn.microsoft.com/D1581B09-06A7-483F-929D-1AF93832942D">RegisterWaitUntilOOBECompleted</a> function as the <i>CallbackContext</i> parameter.


## -returns



This callback function does not return a value.




## -remarks



Once the callback function has completed, <a href="https://msdn.microsoft.com/966803DF-744A-430F-86C0-F6ACA754C603">UnregisterWaitUntilOOBECompleted</a> should be called.



