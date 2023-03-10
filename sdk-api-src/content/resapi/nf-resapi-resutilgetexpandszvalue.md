---
UID: NF:resapi.ResUtilGetExpandSzValue
title: ResUtilGetExpandSzValue function (resapi.h)
description: Returns a expandable string value from the cluster database.
helpviewer_keywords: ["PRESUTIL_GET_EXPAND_SZ_VALUE","PRESUTIL_GET_EXPAND_SZ_VALUE function [Failover Cluster]","ResUtilGetExpandSzValue","ResUtilGetExpandSzValue function [Failover Cluster]","_wolf_resutilgetexpandszvalue","mscs.resutilgetexpandszvalue","resapi/PRESUTIL_GET_EXPAND_SZ_VALUE","resapi/ResUtilGetExpandSzValue"]
old-location: mscs\resutilgetexpandszvalue.htm
tech.root: MsCS
ms.assetid: c0f1064c-d9ae-43af-9622-beae9aee0ce0
ms.date: 12/05/2018
ms.keywords: PRESUTIL_GET_EXPAND_SZ_VALUE, PRESUTIL_GET_EXPAND_SZ_VALUE function [Failover Cluster], ResUtilGetExpandSzValue, ResUtilGetExpandSzValue function [Failover Cluster], _wolf_resutilgetexpandszvalue, mscs.resutilgetexpandszvalue, resapi/PRESUTIL_GET_EXPAND_SZ_VALUE, resapi/ResUtilGetExpandSzValue
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 Enterprise, Windows Server 2003 Datacenter
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
 - ResUtilGetExpandSzValue
 - resapi/ResUtilGetExpandSzValue
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
 - ResUtilGetExpandSzValue
---

# ResUtilGetExpandSzValue function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2003. This function is not exported 
    from ResUtils.dll and programs or DLLs that statically link to it will not load.]

Returns a <a href="/previous-versions/windows/desktop/mscs/e-gly">expandable string</a> value from the 
    <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a>.

## -parameters

### -param hkeyClusterKey [in]

Key identifying the location of the expandable string value in the cluster database.

### -param pszValueName [in]

Pointer to a null-terminated Unicode string containing the name of the value to retrieve.

### -param bExpand [in]

If <b>TRUE</b>, the function expands the string before returning. If 
       <b>FALSE</b>, the string is returned in an expandable form.

## -returns

If the operations succeeds, the function returns a null-terminated Unicode string containing a copy of the 
       specified value.

If the operation fails, the function returns <b>NULL</b>. For more information, see 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

When you are finished with the memory allocated for the value returned by the 
     <b>ResUtilGetExpandSzValue</b> utility function, you 
     must call the function <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> to release it.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregqueryvalue">ClusterRegQueryValue</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetbinaryvalue">ResUtilGetBinaryValue</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetdwordvalue">ResUtilGetDwordValue</a>



<a href="/previous-versions/windows/desktop/api/resapi/nf-resapi-resutilgetmultiszvalue">ResUtilGetMultiSzValue</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetszvalue">ResUtilGetSzValue</a>