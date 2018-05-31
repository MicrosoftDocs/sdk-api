---
UID: NF:combaseapi.CoReleaseServerProcess
title: CoReleaseServerProcess function
author: windows-sdk-content
description: Decrements the global per-process reference count.
old-location: com\coreleaseserverprocess.htm
old-project: com
ms.assetid: b28d41e2-4144-413d-9963-14f2d4dc8876
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: CoReleaseServerProcess, CoReleaseServerProcess function [COM], _com_CoReleaseServerProcess, com.coreleaseserverprocess, combaseapi/CoReleaseServerProcess
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: REGCLS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ole32.dll
-	API-MS-Win-Core-Com-l1-1-0.dll
-	ComBase.dll
-	API-MS-Win-Core-Com-l1-1-1.dll
-	API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
-	CoReleaseServerProcess
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
---

# CoReleaseServerProcess function


## -description


Decrements the global per-process reference count.




## -parameters






## -returns



If the server application should initiate its cleanup, the function returns 0; otherwise, the function returns a nonzero value.




## -remarks



Servers can call <b>CoReleaseServerProcess</b> to decrement a global per-process reference count incremented through a call to <a href="https://msdn.microsoft.com/79887f9d-cad1-492a-b406-d1753ffaf82b">CoAddRefServerProcess</a>.



When that count reaches zero, OLE automatically calls <a href="https://msdn.microsoft.com/a9e526f8-b7c1-47ec-a6ab-91690d93119e">CoSuspendClassObjects</a>, which prevents new activation requests from coming in. This permits the server to deregister its class objects from its various threads without worry that another activation request may come in. New activation requests result in launching a new instance of the local server process.

The simplest way for a local server application to make use of these functions is to call <a href="https://msdn.microsoft.com/79887f9d-cad1-492a-b406-d1753ffaf82b">CoAddRefServerProcess</a> in the constructor for each of its instance objects, and in each of its <a href="https://msdn.microsoft.com/4c817b89-013d-477f-a713-5e320896dfa0">IClassFactory::LockServer</a> methods when the <i>fLock</i> parameter is <b>TRUE</b>. The server application should also call <b>CoReleaseServerProcess</b> in the destructor of each of its instance objects, and in each of its <b>IClassFactory::LockServer</b> methods when the <i>fLock</i> parameter is <b>FALSE</b>. Finally, the server application must check the return code from <b>CoReleaseServerProcess</b>; if it returns 0, the server application should initiate its cleanup. This typically means that a server with multiple threads should signal its various threads to exit their message loops and call <a href="https://msdn.microsoft.com/90b9b9ca-b5b2-48f5-8c2a-b478b6daa7ec">CoRevokeClassObject</a> and <a href="https://msdn.microsoft.com/9411cbed-fa3b-46f7-b677-6ada53324edc">CoUninitialize</a>.

If these APIs are used at all, they must be called in both the object instances and the <a href="https://msdn.microsoft.com/4c817b89-013d-477f-a713-5e320896dfa0">LockServer</a> method, otherwise the server application may be shutdown prematurely. In-process Servers typically should not call <a href="https://msdn.microsoft.com/79887f9d-cad1-492a-b406-d1753ffaf82b">CoAddRefServerProcess</a> or <b>CoReleaseServerProcess</b>.




## -see-also




<a href="https://msdn.microsoft.com/79887f9d-cad1-492a-b406-d1753ffaf82b">CoAddRefServerProcess</a>



<a href="https://msdn.microsoft.com/a9e526f8-b7c1-47ec-a6ab-91690d93119e">CoSuspendClassObjects</a>



<a href="https://msdn.microsoft.com/4c817b89-013d-477f-a713-5e320896dfa0">IClassFactory::LockServer</a>



<a href="https://msdn.microsoft.com/18641a84-56f8-4d27-9ddb-fa64011ac8ba">Out-of-Process Server Implementation Helpers</a>
 

 

