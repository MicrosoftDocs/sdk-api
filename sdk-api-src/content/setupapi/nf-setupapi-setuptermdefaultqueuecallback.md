---
UID: NF:setupapi.SetupTermDefaultQueueCallback
title: SetupTermDefaultQueueCallback function (setupapi.h)
author: windows-sdk-content
description: The SetupTermDefaultQueueCallback function is called after a queue has finished committing. It frees resources allocated by previous calls to SetupInitDefaultQueueCallback or SetupInitDefaultQueueCallbackEx.
old-location: setup\setuptermdefaultqueuecallback.htm
tech.root: SetupApi
ms.assetid: de99ee40-9fbb-42e2-b070-d1c25b238135
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SetupTermDefaultQueueCallback, SetupTermDefaultQueueCallback function [Setup API], _setupapi_setuptermdefaultqueuecallback, setup.setuptermdefaultqueuecallback, setupapi/SetupTermDefaultQueueCallback
ms.topic: function
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
api_name:
 - SetupTermDefaultQueueCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/0a9518b7-f231-48f2-ba50-5b802f8ccaed">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/3ee7da67-42ff-4ea1-9c7f-6c0dcc3dc0b4">SetupInitDefaultQueueCallback</a>



<a href="https://msdn.microsoft.com/9376f55b-55ee-4064-8aed-264c43db0c7d">SetupInitDefaultQueueCallbackEx</a>
 

 

