---
UID: NF:combaseapi.CoFreeUnusedLibrariesEx
title: CoFreeUnusedLibrariesEx function (combaseapi.h)
description: Unloads any DLLs that are no longer in use and whose unload delay has expired.
helpviewer_keywords: ["CoFreeUnusedLibrariesEx","CoFreeUnusedLibrariesEx function [COM]","_com_CoFreeUnusedLibrariesEx","com.cofreeunusedlibrariesex","combaseapi/CoFreeUnusedLibrariesEx"]
old-location: com\cofreeunusedlibrariesex.htm
tech.root: com
ms.assetid: 01660e9d-d8f2-40ef-a6d6-b80f0140ab5f
ms.date: 12/05/2018
ms.keywords: CoFreeUnusedLibrariesEx, CoFreeUnusedLibrariesEx function [COM], _com_CoFreeUnusedLibrariesEx, com.cofreeunusedlibrariesex, combaseapi/CoFreeUnusedLibrariesEx
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
req.dll: ComBase.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CoFreeUnusedLibrariesEx
 - combaseapi/CoFreeUnusedLibrariesEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - ComBase.dll
 - ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoFreeUnusedLibrariesEx
---

## -description

Unloads any DLLs that are no longer in use and whose unload delay has expired.

## -parameters

### -param dwUnloadDelay [in]

The delay in milliseconds between the time that the DLL has stated it can be unloaded until it becomes a candidate to unload. Setting this parameter to INFINITE uses the system default delay (10 minutes). Setting this parameter to 0 forces the unloading of any DLLs without any delay.

### -param dwReserved [in]

This parameter is reserved and must be 0.

## -remarks

COM supplies functions to reclaim memory held by DLLs containing components. The most commonly used function is <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibraries">CoFreeUnusedLibraries</a>. <b>CoFreeUnusedLibraries</b> does not immediately release DLLs that have no active object. There is a 10-minute delay for multithreaded apartments (MTAs) and neutral apartments (NAs). For single-threaded apartments (STAs), there is no delay.



The 10-minute delay for <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibraries">CoFreeUnusedLibraries</a> is to avoid multithread race conditions caused by unloading a component DLL. This default delay may be too long for many applications.



COM maintains a list of active DLLs that have had components loaded for the apartments that can be hosted on the thread where this function is called. When <b>CoFreeUnusedLibrariesEx</b> is called, each DLL on that list has its <a href="/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow">DllCanUnloadNow</a> function called. If <b>DllCanUnloadNow</b> returns S_FALSE (or is not exported), this DLL is not ready to be unloaded. If <b>DllCanUnloadNow</b> returns S_OK, this DLL is moved off the active list to a "candidate-for-unloading" list.



Adding the DLL to the candidate-for-unloading list time-stamps the DLL <i>dwUnloadDelay</i> milliseconds from when this move occurs. When <b>CoFreeUnusedLibrariesEx</b> (or <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibraries">CoFreeUnusedLibraries</a>) is called again, at least <i>dwUnloadDelay</i> milliseconds from the call that moved the DLL to the candidate-for-unloading list, the DLL is actually freed from memory. If COM uses the component DLL while the DLL is on the candidate-for-unloading list, it is moved back to the active list.



Setting <i>dwUnloadDelay</i> to 0 may have unexpected consequences. The component DLL may need some time for cleanup after it returns from the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow">DllCanUnloadNow</a> function. For example, if the DLL had its own worker threads, using a value of 0 would most likely lead to a problem because the code executing on these threads would be unmapped, caused by the unloading of the DLL before the worker threads have a chance to exit. Also, using too brief of a value for <i>dwUnloadDelay</i> can lead to performance issues because there is more overhead in reloading a DLL than letting it page out.

This behavior is triggered by the DLL supplying components with threading models set to Free, Neutral, or Both. For a threading model set to Apartment (or if no threading model is specified), <i>dwUnloadDelay</i> is treated as 0 because these components are tied to the single thread hosting the apartment.

## -see-also

<a href="/windows/desktop/api/objbase/nf-objbase-cofreealllibraries">CoFreeAllLibraries</a>



<a href="/windows/desktop/api/objbase/nf-objbase-cofreelibrary">CoFreeLibrary</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibraries">CoFreeUnusedLibraries</a>



<a href="/windows/desktop/api/objbase/nf-objbase-coloadlibrary">CoLoadLibrary</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow">DllCanUnloadNow</a>