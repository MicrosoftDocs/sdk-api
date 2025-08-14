---
UID: NF:combaseapi.CoAddRefServerProcess
title: CoAddRefServerProcess function (combaseapi.h)
description: Increments a global per-process reference count.
helpviewer_keywords: ["CoAddRefServerProcess","CoAddRefServerProcess function [COM]","_com_CoAddRefServerProcess","com.coaddrefserverprocess","combaseapi/CoAddRefServerProcess"]
old-location: com\coaddrefserverprocess.htm
tech.root: com
ms.assetid: 79887f9d-cad1-492a-b406-d1753ffaf82b
ms.date: 12/05/2018
ms.keywords: CoAddRefServerProcess, CoAddRefServerProcess function [COM], _com_CoAddRefServerProcess, com.coaddrefserverprocess, combaseapi/CoAddRefServerProcess
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
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CoAddRefServerProcess
 - combaseapi/CoAddRefServerProcess
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-downlevel-ole32-l1-1-0.dll
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoAddRefServerProcess
---

# CoAddRefServerProcess function


## -description

Increments a global per-process reference count.



## -returns

The current reference count.

## -remarks

Servers can call <b>CoAddRefServerProcess</b> to increment a global per-process reference count. This function is particularly helpful to servers that are implemented with multiple threads, either multi-apartmented or free-threaded. Servers of these types must coordinate the decision to shut down with activation requests across multiple threads. Calling <b>CoAddRefServerProcess</b> increments a global per-process reference count, and calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess">CoReleaseServerProcess</a> decrements that count.

When that count reaches zero, OLE automatically calls <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cosuspendclassobjects">CoSuspendClassObjects</a>, which prevents new activation requests from coming in. This permits the server to deregister its class objects from its various threads without worry that another activation request may come in. New activation requests result in launching a new instance of the local server process.

The simplest way for a local server application to make use of these functions is to call <b>CoAddRefServerProcess</b> in the constructor for each of its instance objects, and in each of its <a href="/windows/desktop/api/unknwnbase/nf-unknwnbase-iclassfactory-lockserver">IClassFactory::LockServer</a> methods when the <i>fLock</i> parameter is <b>TRUE</b>. The server application should also call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess">CoReleaseServerProcess</a> in the destruction of each of its instance objects, and in each of its <b>LockServer</b> methods when the <i>fLock</i> parameter is <b>FALSE</b>. Finally, the server application should pay attention to the return code from <b>CoReleaseServerProcess</b> and if it returns 0, the server application should initiate its cleanup, which, for a server with multiple threads, typically means that it should signal its various threads to exit their message loops and call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-corevokeclassobject">CoRevokeClassObject</a> and <a href="/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize">CoUninitialize</a>.

If these functions are used at all, they must be called in both the object instances and the <a href="/windows/desktop/api/unknwnbase/nf-unknwnbase-iclassfactory-lockserver">LockServer</a> method, otherwise the server application may be shut down prematurely. In-process servers typically should not call <b>CoAddRefServerProcess</b> or <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess">CoReleaseServerProcess</a>.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess">CoReleaseServerProcess</a>



<a href="/windows/desktop/api/unknwnbase/nf-unknwnbase-iclassfactory-lockserver">IClassFactory::LockServer</a>



<a href="/windows/desktop/com/out-of-process-server-implementation-helpers">Out-of-Process Server Implementation Helpers</a>
