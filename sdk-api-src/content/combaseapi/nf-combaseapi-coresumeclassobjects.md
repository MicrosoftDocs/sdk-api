---
UID: NF:combaseapi.CoResumeClassObjects
title: CoResumeClassObjects function (combaseapi.h)
description: Called by a server that can register multiple class objects to inform the SCM about all registered classes, and permits activation requests for those class objects.
helpviewer_keywords: ["CoResumeClassObjects","CoResumeClassObjects function [COM]","_com_CoResumeClassObjects","com.coresumeclassobjects","combaseapi/CoResumeClassObjects"]
old-location: com\coresumeclassobjects.htm
tech.root: com
ms.assetid: c2b6e8d8-99a1-4af3-9881-bfe6932e4a76
ms.date: 12/05/2018
ms.keywords: CoResumeClassObjects, CoResumeClassObjects function [COM], _com_CoResumeClassObjects, com.coresumeclassobjects, combaseapi/CoResumeClassObjects
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - CoResumeClassObjects
 - combaseapi/CoResumeClassObjects
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
 - CoResumeClassObjects
---

# CoResumeClassObjects function


## -description

Called by a server that can register multiple class objects to inform the SCM about all registered classes, and permits activation requests for those class objects.



## -returns

This function returns S_OK to indicate that the CLSID was retrieved successfully.

## -remarks

Servers that can register multiple class objects call <b>CoResumeClassObjects</b> once, after having first called <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject">CoRegisterClassObject</a>, specifying REGCLS_LOCAL_SERVER | REGCLS_SUSPENDED for each CLSID the server supports. This function causes OLE to inform the SCM about all the registered classes, and begins letting activation requests into the server process.

This reduces the overall registration time, and thus the server application startup time, by making a single call to the SCM, no matter how many CLSIDs are registered for the server. Another advantage is that if the server has multiple apartments with different CLSIDs registered in different apartments, or is a free-threaded server, no activation requests will come in until the server calls <b>CoResumeClassObjects</b>. This gives the server a chance to register all of its CLSIDs and get properly set up before having to deal with activation requests, and possibly shutdown requests.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject">CoRegisterClassObject</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cosuspendclassobjects">CoSuspendClassObjects</a>



<a href="/windows/desktop/com/out-of-process-server-implementation-helpers">Out-of-Process Server Implementation Helpers</a>
