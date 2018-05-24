---
UID: NF:objidl.ISurrogateService.ApplicationFree
title: ISurrogateService::ApplicationFree
author: windows-driver-content
description: Releases the application.
old-location: com\isurrogateservice_applicationfree.htm
old-project: com
ms.assetid: 703de030-ac99-4673-8399-695116bf07d5
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: ApplicationFree, ApplicationFree method [COM], ApplicationFree method [COM],ISurrogateService interface, ISurrogateService interface [COM],ApplicationFree method, ISurrogateService.ApplicationFree, ISurrogateService::ApplicationFree, _com_isurrogateservice_applicationfree, com.isurrogateservice_applicationfree, objidl/ISurrogateService::ApplicationFree
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
-	ISurrogateService.ApplicationFree
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISurrogateService::ApplicationFree


## -description


Releases the application.


## -parameters




### -param rguidApplID [in]

The application identifier.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, it is E_UNEXPECTED.




## -see-also




<a href="https://msdn.microsoft.com/d1ffee1d-f907-4091-b993-cf13d8ce616c">CoGetInterceptor</a>



<a href="https://msdn.microsoft.com/56a75123-f402-4187-af13-d31f72a5f094">ICallFrame</a>



<a href="https://msdn.microsoft.com/2f1e1b8d-6150-45e9-89e2-524d80df558d">ICallFrameEvents</a>



<a href="https://msdn.microsoft.com/d0a72c87-598b-4ebe-bc93-65e0927a4c3d">ICallInterceptor</a>



<a href="https://msdn.microsoft.com/66de8d71-c27c-41bd-a741-02de5c779290">ICallUnmarshal</a>



<a href="https://msdn.microsoft.com/01773aa6-3eb5-43dd-8a10-d1351a07fe1f">ISurrogateService</a>
 

 

