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

# RemoveSecureMemoryCacheCallback function


## -description


Unregisters a callback function that was previously registered with the <a href="https://msdn.microsoft.com/6c89d6f3-182e-4b10-931c-8d55d603c9dc">AddSecureMemoryCacheCallback</a> function.


## -parameters




### -param pfnCallBack [in]

A pointer to the application-defined <a href="https://msdn.microsoft.com/abde4b6f-7cd8-4a4b-9b00-f035b2c29054">SecureMemoryCacheCallback</a> function to remove.


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>.




## -remarks



To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or later. For more information, see <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/6c89d6f3-182e-4b10-931c-8d55d603c9dc">AddSecureMemoryCacheCallback</a>



<a href="https://msdn.microsoft.com/abde4b6f-7cd8-4a4b-9b00-f035b2c29054">SecureMemoryCacheCallback</a>
 

 

