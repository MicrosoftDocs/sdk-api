---
UID: NF:combaseapi.CoGetCurrentProcess
title: CoGetCurrentProcess function (combaseapi.h)
description: Returns a value that is unique to the current thread. CoGetCurrentProcess can be used to avoid thread ID reuse problems.
helpviewer_keywords: ["CoGetCurrentProcess","CoGetCurrentProcess function [COM]","_com_CoGetCurrentProcess","com.cogetcurrentprocess","combaseapi/CoGetCurrentProcess"]
old-location: com\cogetcurrentprocess.htm
tech.root: com
ms.assetid: 46b0448f-f1c5-4da7-8489-bbd6d0fab79e
ms.date: 12/05/2018
ms.keywords: CoGetCurrentProcess, CoGetCurrentProcess function [COM], _com_CoGetCurrentProcess, com.cogetcurrentprocess, combaseapi/CoGetCurrentProcess
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
 - CoGetCurrentProcess
 - combaseapi/CoGetCurrentProcess
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
 - CoGetCurrentProcess
---

# CoGetCurrentProcess function


## -description

Returns a value that is unique to the current thread. <b>CoGetCurrentProcess</b> can be used to avoid thread ID reuse problems.



## -returns

The function returns the unique identifier of the current thread.

## -remarks

Using the value returned from a call to <b>CoGetCurrentProcess</b> can help you in maintaining tables that are keyed by threads or in uniquely identifying a thread to other threads or processes.

<b>CoGetCurrentProcess</b> returns a value that is effectively unique, because it is not used again until 2³² more threads have been created on the current workstation or until the workstation is restarted.

The value returned by <b>CoGetCurrentProcess</b> will uniquely identify the same thread for the life of the caller. Because thread IDs can be reused without notice as threads are created and destroyed, this value is more reliable than the value returned by the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid">GetCurrentThreadId</a> function.
