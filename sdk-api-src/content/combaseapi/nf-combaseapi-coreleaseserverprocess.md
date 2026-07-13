---
UID: NF:combaseapi.CoReleaseServerProcess
title: CoReleaseServerProcess function (combaseapi.h)
description: Decrements the global per-process reference count.
helpviewer_keywords: ["CoReleaseServerProcess","CoReleaseServerProcess function [COM]","_com_CoReleaseServerProcess","com.coreleaseserverprocess","combaseapi/CoReleaseServerProcess"]
old-location: com\coreleaseserverprocess.htm
tech.root: com
ms.assetid: b28d41e2-4144-413d-9963-14f2d4dc8876
ms.date: 12/05/2018
ms.keywords: CoReleaseServerProcess, CoReleaseServerProcess function [COM], _com_CoReleaseServerProcess, com.coreleaseserverprocess, combaseapi/CoReleaseServerProcess
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
 - CoReleaseServerProcess
 - combaseapi/CoReleaseServerProcess
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
 - CoReleaseServerProcess
---

# CoReleaseServerProcess function


## -description

Decrements the global per-process reference count.



## -returns

If the server application should initiate its cleanup, the function returns 0; otherwise, the function returns a nonzero value.

## -remarks

Servers can call <b>CoReleaseServerProcess</b> to decrement a global per-process reference count incremented through a call to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coaddrefserverprocess">CoAddRefServerProcess</a>.



When that count reaches zero, OLE automatically calls <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cosuspendclassobjects">CoSuspendClassObjects</a>, which prevents new activation requests from coming in. This permits the server to deregister its class objects from its various threads without worry that another activation request may come in. New activation requests result in launching a new instance of the local server process.

The simplest way for a local server application to make use of these functions is to call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coaddrefserverprocess">CoAddRefServerProcess</a> in the constructor for each of its instance objects, and in each of its <a href="/windows/desktop/api/unknwnbase/nf-unknwnbase-iclassfactory-lockserver">IClassFactory::LockServer</a> methods when the <i>fLock</i> parameter is <b>TRUE</b>. The server application should also call <b>CoReleaseServerProcess</b> in the destructor of each of its instance objects, and in each of its <b>IClassFactory::LockServer</b> methods when the <i>fLock</i> parameter is <b>FALSE</b>. Finally, the server application must check the return code from <b>CoReleaseServerProcess</b>; if it returns 0, the server application should initiate its cleanup. This typically means that a server with multiple threads should signal its various threads to exit their message loops and call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-corevokeclassobject">CoRevokeClassObject</a> and <a href="/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize">CoUninitialize</a>.

If these APIs are used at all, they must be called in both the object instances and the <a href="/windows/desktop/api/unknwnbase/nf-unknwnbase-iclassfactory-lockserver">LockServer</a> method, otherwise the server application may be shutdown prematurely. In-process Servers typically should not call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coaddrefserverprocess">CoAddRefServerProcess</a> or <b>CoReleaseServerProcess</b>.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-coaddrefserverprocess">CoAddRefServerProcess</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cosuspendclassobjects">CoSuspendClassObjects</a>



<a href="/windows/desktop/api/unknwnbase/nf-unknwnbase-iclassfactory-lockserver">IClassFactory::LockServer</a>



<a href="/windows/desktop/com/out-of-process-server-implementation-helpers">Out-of-Process Server Implementation Helpers</a>
