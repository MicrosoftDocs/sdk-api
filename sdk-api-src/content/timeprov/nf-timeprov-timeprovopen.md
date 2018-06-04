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

# TimeProvOpen function


## -description


A callback function that is called by the time provider manager when the time provider DLL is loaded.


## -parameters




### -param wszName [in]

The provider name.


### -param pSysCallbacks [in]

A pointer to a 
<a href="https://msdn.microsoft.com/a38f8b26-9450-4033-bdd7-e73726c2d609">TimeProvSysCallbacks</a> structure that specifies pointers to the functions provided by the time service to the time provider. The system allocates this structure, and it is destroyed when the function returns. Therefore, you must copy the information to another buffer.


### -param phTimeProv [out]

A pointer to a buffer that contains a handle to the provider. The time provider manager uses this handle to communicate with the time provider.


## -returns



If the function succeeds, the return value is S_OK. Otherwise, the return value is one of the error codes defined in WinError.h.




## -remarks



You should return from this callback function as quickly as possible. Perform any initialization in another thread.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/6be08c49-be68-4b75-b740-fc1d5a2ff592">Sample Time Provider</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/f90da019-072e-46c9-8e05-0321a9960968">AlertSamplesAvailFunc</a>



<a href="https://msdn.microsoft.com/e1b527e2-ab7c-4106-b203-e74b4ce2a89b">GetTimeSysInfoFunc</a>



<a href="https://msdn.microsoft.com/ddaea389-3f58-4011-bcf8-c60546d1bce1">LogTimeProvEventFunc</a>



<a href="https://msdn.microsoft.com/e52dd1d3-081a-4fcc-85d9-a1dcef0e8011">SetProviderStatusFunc</a>



<a href="https://msdn.microsoft.com/a38f8b26-9450-4033-bdd7-e73726c2d609">TimeProvSysCallbacks</a>
 

 

