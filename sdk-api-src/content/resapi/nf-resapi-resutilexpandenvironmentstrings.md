---
UID: NF:resapi.ResUtilExpandEnvironmentStrings
title: ResUtilExpandEnvironmentStrings function (resapi.h)
author: windows-sdk-content
description: Expands strings containing unexpanded references to environment variables. The PRESUTIL_EXPAND_ENVIRONMENT_STRINGS type defines a pointer to this function.
old-location: mscs\resutilexpandenvironmentstrings.htm
tech.root: MsCS
ms.assetid: 633e49f5-e01c-4cbd-a2ef-61fcb9e192f4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PRESUTIL_EXPAND_ENVIRONMENT_STRINGS, PRESUTIL_EXPAND_ENVIRONMENT_STRINGS function [Failover Cluster], ResUtilExpandEnvironmentStrings, ResUtilExpandEnvironmentStrings function [Failover Cluster], _wolf_resutilexpandenvironmentstrings, mscs.resutilexpandenvironmentstrings, resapi/PRESUTIL_EXPAND_ENVIRONMENT_STRINGS, resapi/ResUtilExpandEnvironmentStrings
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
ms.custom: 19H1
---

# ResUtilExpandEnvironmentStrings function


## -description


Expands strings containing unexpanded references to environment variables. The <b>PRESUTIL_EXPAND_ENVIRONMENT_STRINGS</b> type defines a pointer to this function.


## -parameters




### -param pszSrc [in]

Pointer to a null-terminated Unicode string containing unexpanded references to environment variables (an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/e-gly">expandable string</a>).


## -returns



If the operation succeeds, the function returns a pointer to the expanded string (REG_EXPAND_SZ). The function allocates the necessary memory with <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a>. To prevent memory leaks, be sure to release the memory with <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a>.

If the operation fails, the function returns <b>NULL</b>.
     For more information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/resapi/nf-resapi-resutilfindexpandszproperty">ResUtilFindExpandSzProperty</a>



<a href="https://docs.microsoft.com/windows/desktop/api/resapi/nf-resapi-resutilgetenvironmentwithnetname">ResUtilGetEnvironmentWithNetName</a>



<a href="https://docs.microsoft.com/windows/desktop/api/resapi/nc-resapi-presutil_get_expand_sz_value">ResUtilGetExpandSzValue</a>
 

 

