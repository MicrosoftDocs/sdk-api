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

# SetupTermDefaultQueueCallback function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupTermDefaultQueueCallback</b> function is called after a queue has finished committing. It frees resources allocated by previous calls to 
<a href="https://msdn.microsoft.com/3ee7da67-42ff-4ea1-9c7f-6c0dcc3dc0b4">SetupInitDefaultQueueCallback</a> or 
<a href="https://msdn.microsoft.com/9376f55b-55ee-4064-8aed-264c43db0c7d">SetupInitDefaultQueueCallbackEx</a>.


## -parameters




### -param Context [in]

Pointer to the context used by the default callback routine.


## -returns



Does not return a value.

To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Regardless of whether you initialized the context used by the default queue callback routine with 
<a href="https://msdn.microsoft.com/3ee7da67-42ff-4ea1-9c7f-6c0dcc3dc0b4">SetupInitDefaultQueueCallback</a> or 
<a href="https://msdn.microsoft.com/9376f55b-55ee-4064-8aed-264c43db0c7d">SetupInitDefaultQueueCallbackEx</a>, after the queued operations have finished processing, call 
<b>SetupTermDefaultQueueCallback</b> to release the resources allocated in initializing the context structure. For more information see 
<a href="https://msdn.microsoft.com/e25a9787-a4a3-4d06-bf55-f6f7cfb23481">Initializing and Terminating the Callback Context</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/3ee7da67-42ff-4ea1-9c7f-6c0dcc3dc0b4">SetupInitDefaultQueueCallback</a>



<a href="https://msdn.microsoft.com/9376f55b-55ee-4064-8aed-264c43db0c7d">SetupInitDefaultQueueCallbackEx</a>
 

 

