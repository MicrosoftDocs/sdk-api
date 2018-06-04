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

# ImagehlpApiVersionEx function


## -description


Modifies the version information of the library used by the application.


## -parameters




### -param AppVersion [in]

A pointer to an 
<a href="https://msdn.microsoft.com/f983f639-6a94-4b83-a443-0d98b85d3950">API_VERSION</a> structure that contains valid version information for your application.


## -returns




						The return value is a pointer to an 
<a href="https://msdn.microsoft.com/f983f639-6a94-4b83-a443-0d98b85d3950">API_VERSION</a> structure.
					




## -remarks



Use the 
<b>ImagehlpApiVersionEx</b> function to indicate the version of the library with which the application was built. The library uses this information to ensure compatibility. For example, consider walking through kernel-mode callback stack frames (User and GDI exist in kernel mode). If you call 
<b>ImagehlpApiVersionEx</b> to set the <b>Revision</b> member to version 4 or later, the 
<a href="https://msdn.microsoft.com/e2bdaa4c-5474-41a0-bcea-927570c8402c">StackWalk64</a> function will continue through a callback stack frame. Otherwise, if you set <b>Revision</b> to a version earlier than 4, 
<b>StackWalk64</b> will stop at the kernel transition.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.




## -see-also




<a href="https://msdn.microsoft.com/f983f639-6a94-4b83-a443-0d98b85d3950">API_VERSION</a>



<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/0ad9a047-f2ae-4fbe-8a85-9817a616ef73">ImagehlpApiVersion</a>
 

 

