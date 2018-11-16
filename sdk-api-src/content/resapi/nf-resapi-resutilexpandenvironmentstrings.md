---
UID: NF:resapi.ResUtilExpandEnvironmentStrings
title: ResUtilExpandEnvironmentStrings function
author: windows-sdk-content
description: Expands strings containing unexpanded references to environment variables. The PRESUTIL_EXPAND_ENVIRONMENT_STRINGS type defines a pointer to this function.
old-location: mscs\resutilexpandenvironmentstrings.htm
tech.root: MsCS
ms.assetid: 633e49f5-e01c-4cbd-a2ef-61fcb9e192f4
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: PRESUTIL_EXPAND_ENVIRONMENT_STRINGS, PRESUTIL_EXPAND_ENVIRONMENT_STRINGS function [Failover Cluster], ResUtilExpandEnvironmentStrings, ResUtilExpandEnvironmentStrings function [Failover Cluster], _wolf_resutilexpandenvironmentstrings, mscs.resutilexpandenvironmentstrings, resapi/PRESUTIL_EXPAND_ENVIRONMENT_STRINGS, resapi/ResUtilExpandEnvironmentStrings
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ResUtils.lib
req.dll: ResUtils.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ResUtils.dll
api_name:
 - ResUtilExpandEnvironmentStrings
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ResUtilExpandEnvironmentStrings
: 
---

# ResUtilExpandEnvironmentStrings function


## -description


Expands strings containing unexpanded references to environment variables. The <b>PRESUTIL_EXPAND_ENVIRONMENT_STRINGS</b> type defines a pointer to this function.


## -parameters




### -param pszSrc [in]

Pointer to a null-terminated Unicode string containing unexpanded references to environment variables (an <a href="https://msdn.microsoft.com/en-us/library/Aa369570(v=VS.85).aspx">expandable string</a>).


## -returns



If the operation succeeds, the function returns a pointer to the expanded string (REG_EXPAND_SZ). The function allocates the necessary memory with <a href="https://msdn.microsoft.com/da8cd2be-ff4c-4da5-813c-8759a58228c9">LocalAlloc</a>. To prevent memory leaks, be sure to release the memory with <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a>.

If the operation fails, the function returns <b>NULL</b>.
     For more information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/44fb21bd-6cc2-4b1b-ae8f-c977fa336747">ResUtilFindExpandSzProperty</a>



<a href="https://msdn.microsoft.com/683235ac-153d-4442-915e-e1bf9b5e8810">ResUtilGetEnvironmentWithNetName</a>



<a href="https://msdn.microsoft.com/c0f1064c-d9ae-43af-9622-beae9aee0ce0">ResUtilGetExpandSzValue</a>
 

 

