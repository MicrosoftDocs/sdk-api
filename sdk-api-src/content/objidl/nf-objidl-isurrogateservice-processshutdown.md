---
UID: NF:objidl.ISurrogateService.ProcessShutdown
title: ISurrogateService::ProcessShutdown
author: windows-driver-content
description: Shuts down the process.
old-location: com\isurrogateservice_processshutdown.htm
old-project: com
ms.assetid: b01dc079-647c-4e58-a36b-0a665355afb7
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: ISurrogateService interface [COM],ProcessShutdown method, ISurrogateService.ProcessShutdown, ISurrogateService::ProcessShutdown, ProcessShutdown, ProcessShutdown method [COM], ProcessShutdown method [COM],ISurrogateService interface, _com_isurrogateservice_processshutdown, com.isurrogateservice_processshutdown, objidl/ISurrogateService::ProcessShutdown
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ObjIdl.h
api_name:
-	ISurrogateService.ProcessShutdown
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ISurrogateService::ProcessShutdown


## -description


Shuts down the process.


## -parameters




### -param shutdownType [in]

The shutdown type, as described in Remarks.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, it is E_UNEXPECTED.




## -remarks



The shutdown type is defined by the following enum.

<pre class="syntax" xml:space="preserve"><code>typedef enum tagShutdownType { 
    IdleShutdown, 
    ForcedShutdown
} ShutdownType;
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/d1ffee1d-f907-4091-b993-cf13d8ce616c">CoGetInterceptor</a>



<a href="https://msdn.microsoft.com/56a75123-f402-4187-af13-d31f72a5f094">ICallFrame</a>



<a href="https://msdn.microsoft.com/2f1e1b8d-6150-45e9-89e2-524d80df558d">ICallFrameEvents</a>



<a href="https://msdn.microsoft.com/d0a72c87-598b-4ebe-bc93-65e0927a4c3d">ICallInterceptor</a>



<a href="https://msdn.microsoft.com/66de8d71-c27c-41bd-a741-02de5c779290">ICallUnmarshal</a>



<a href="https://msdn.microsoft.com/01773aa6-3eb5-43dd-8a10-d1351a07fe1f">ISurrogateService</a>
 

 

