---
UID: NF:combaseapi.CoSuspendClassObjects
title: CoSuspendClassObjects function (combaseapi.h)
author: windows-sdk-content
description: Prevents any new activation requests from the SCM on all class objects registered within the process.
old-location: com\cosuspendclassobjects.htm
tech.root: com
ms.assetid: a9e526f8-b7c1-47ec-a6ab-91690d93119e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CoSuspendClassObjects, CoSuspendClassObjects function [COM], _com_CoSuspendClassObjects, com.cosuspendclassobjects, combaseapi/CoSuspendClassObjects
ms.topic: function
f1_keywords: 
 - "combaseapi/CoSuspendClassObjects"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoSuspendClassObjects
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CoSuspendClassObjects function


## -description


Prevents any new activation requests from the SCM on all class objects registered within the process.


## -parameters






## -returns



This function returns S_OK to indicate that the activation of class objects was successfully suspended.




## -remarks



<b>CoSuspendClassObjects</b> prevents any new activation requests from the SCM on all class objects registered within the process. Even though a process may call this function, the process still must call the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-corevokeclassobject">CoRevokeClassObject</a> function for each CLSID it has registered, in the apartment it registered in. Applications typically do not need to call this function, which is generally only called internally by OLE when used in conjunction with the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess">CoReleaseServerProcess</a> function.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess">CoReleaseServerProcess</a>



<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-corevokeclassobject">CoRevokeClassObject</a>



<a href="https://docs.microsoft.com/windows/desktop/com/out-of-process-server-implementation-helpers">Out-of-Process Server Implementation Helpers</a>
 

 

