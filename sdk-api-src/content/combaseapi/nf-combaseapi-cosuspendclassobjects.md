---
UID: NF:combaseapi.CoSuspendClassObjects
title: CoSuspendClassObjects function (combaseapi.h)
description: Prevents any new activation requests from the SCM on all class objects registered within the process.
helpviewer_keywords: ["CoSuspendClassObjects","CoSuspendClassObjects function [COM]","_com_CoSuspendClassObjects","com.cosuspendclassobjects","combaseapi/CoSuspendClassObjects"]
old-location: com\cosuspendclassobjects.htm
tech.root: com
ms.assetid: a9e526f8-b7c1-47ec-a6ab-91690d93119e
ms.date: 12/05/2018
ms.keywords: CoSuspendClassObjects, CoSuspendClassObjects function [COM], _com_CoSuspendClassObjects, com.cosuspendclassobjects, combaseapi/CoSuspendClassObjects
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
 - CoSuspendClassObjects
 - combaseapi/CoSuspendClassObjects
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
 - CoSuspendClassObjects
---

# CoSuspendClassObjects function


## -description

Prevents any new activation requests from the SCM on all class objects registered within the process.



## -returns

This function returns S_OK to indicate that the activation of class objects was successfully suspended.

## -remarks

<b>CoSuspendClassObjects</b> prevents any new activation requests from the SCM on all class objects registered within the process. Even though a process may call this function, the process still must call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-corevokeclassobject">CoRevokeClassObject</a> function for each CLSID it has registered, in the apartment it registered in. Applications typically do not need to call this function, which is generally only called internally by OLE when used in conjunction with the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess">CoReleaseServerProcess</a> function.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess">CoReleaseServerProcess</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-corevokeclassobject">CoRevokeClassObject</a>



<a href="/windows/desktop/com/out-of-process-server-implementation-helpers">Out-of-Process Server Implementation Helpers</a>
