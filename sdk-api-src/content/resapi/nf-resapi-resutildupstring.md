---
UID: NF:resapi.ResUtilDupString
title: ResUtilDupString function (resapi.h)
description: Duplicates a null-terminated Unicode string.
helpviewer_keywords: ["PRESUTIL_DUP_STRING","PRESUTIL_DUP_STRING function [Failover Cluster]","ResUtilDupString","ResUtilDupString function [Failover Cluster]","_wolf_resutildupstring","mscs.resutildupstring","resapi/PRESUTIL_DUP_STRING","resapi/ResUtilDupString"]
old-location: mscs\resutildupstring.htm
tech.root: MsCS
ms.assetid: 7d993247-ea8c-46a0-a11e-e03b981ed4ae
ms.date: 12/05/2018
ms.keywords: PRESUTIL_DUP_STRING, PRESUTIL_DUP_STRING function [Failover Cluster], ResUtilDupString, ResUtilDupString function [Failover Cluster], _wolf_resutildupstring, mscs.resutildupstring, resapi/PRESUTIL_DUP_STRING, resapi/ResUtilDupString
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ResUtilDupString
 - resapi/ResUtilDupString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ResUtils.dll
api_name:
 - ResUtilDupString
---

# ResUtilDupString function


## -description

Duplicates a null-terminated Unicode string.

## -parameters

### -param pszInString [in]

Pointer to the string to duplicate.

## -returns

If the operation succeeds, the function returns a pointer to a buffer containing the duplicate string.

If the operation fails, 
the function returns <b>NULL</b>. For more information, call the function  <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

With the  <b>ResUtilDupString</b> utility function, after using the returned string, callers should deallocate the buffer by calling the function  <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a>.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a>