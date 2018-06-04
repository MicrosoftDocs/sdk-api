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

# TimeProvClose function


## -description


A  callback function that is called by the time provider manager to shut down the time provider.


## -parameters




### -param hTimeProv [in]

A handle to the time provider. The 
<a href="https://msdn.microsoft.com/cf4f8d00-4c6f-4036-a179-444ff7505ab4">TimeProvOpen</a> function receives this handle.


## -returns



If the function succeeds, the return value is S_OK. Otherwise, the return value is one of the error codes defined in WinError.h.




## -remarks



The provider should clean up its resources and terminate its operation. When the function returns, the time provider manager can unload the DLL. Therefore, the handle to the time provider is no longer valid and should not be used again.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/6be08c49-be68-4b75-b740-fc1d5a2ff592">Sample Time Provider</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/cf4f8d00-4c6f-4036-a179-444ff7505ab4">TimeProvOpen</a>
 

 

