---
UID: NF:objidl.ISurrogateService.Init
title: ISurrogateService::Init
author: windows-sdk-content
description: Initializes the process server.
old-location: com\isurrogateservice_init.htm
old-project: com
ms.assetid: ed2e628c-5c86-48fd-aa55-f532602247ea
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ISurrogateService interface [COM],Init method, ISurrogateService.Init, ISurrogateService::Init, Init, Init method [COM], Init method [COM],ISurrogateService interface, _com_isurrogateservice_init, com.isurrogateservice_init, objidl/ISurrogateService::Init
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: objidl.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - ISurrogateService.Init
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ISurrogateService::Init


## -description


Initializes the process server.


## -parameters




### -param rguidProcessID [in]

The process ID of the server application.


### -param pProcessLock [in]

A pointer to an instance of the <a href="https://msdn.microsoft.com/49ec5657-d54e-4af7-8c20-00de383ecf89">IProcessLock</a> interface.


### -param pfApplicationAware [out]

Indicates whether the application is aware of the initialization.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, it is E_UNEXPECTED.




## -see-also




<a href="https://msdn.microsoft.com/d1ffee1d-f907-4091-b993-cf13d8ce616c">CoGetInterceptor</a>



<a href="https://msdn.microsoft.com/56a75123-f402-4187-af13-d31f72a5f094">ICallFrame</a>



<a href="https://msdn.microsoft.com/2f1e1b8d-6150-45e9-89e2-524d80df558d">ICallFrameEvents</a>



<a href="https://msdn.microsoft.com/d0a72c87-598b-4ebe-bc93-65e0927a4c3d">ICallInterceptor</a>



<a href="https://msdn.microsoft.com/66de8d71-c27c-41bd-a741-02de5c779290">ICallUnmarshal</a>



<a href="https://msdn.microsoft.com/01773aa6-3eb5-43dd-8a10-d1351a07fe1f">ISurrogateService</a>
 

 

