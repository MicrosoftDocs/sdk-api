---
UID: NF:resapi.ResUtilGetSzValue
title: ResUtilGetSzValue function (resapi.h)
description: Returns a string value from the cluster database.
helpviewer_keywords: ["PRESUTIL_GET_SZ_VALUE","PRESUTIL_GET_SZ_VALUE function [Failover Cluster]","ResUtilGetSzValue","ResUtilGetSzValue function [Failover Cluster]","_wolf_resutilgetszvalue","mscs.resutilgetszvalue","resapi/PRESUTIL_GET_SZ_VALUE","resapi/ResUtilGetSzValue"]
old-location: mscs\resutilgetszvalue.htm
tech.root: MsCS
ms.assetid: c2ba04ea-0f98-4513-b8f8-658056a493e6
ms.date: 12/05/2018
ms.keywords: PRESUTIL_GET_SZ_VALUE, PRESUTIL_GET_SZ_VALUE function [Failover Cluster], ResUtilGetSzValue, ResUtilGetSzValue function [Failover Cluster], _wolf_resutilgetszvalue, mscs.resutilgetszvalue, resapi/PRESUTIL_GET_SZ_VALUE, resapi/ResUtilGetSzValue
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
 - ResUtilGetSzValue
 - resapi/ResUtilGetSzValue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-cluster-resutils-l1-1-3.dll
 - ResUtils.dll
api_name:
 - ResUtilGetSzValue
---

# ResUtilGetSzValue function


## -description

Returns a string value from the  <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a>.

## -parameters

### -param hkeyClusterKey [in]

Key identifying the location of the value in the cluster database.

### -param pszValueName [in]

A null-terminated Unicode string containing the name of the value to retrieve.

## -returns

If the operation succeeds, 
the function returns a pointer to a buffer containing the string value.

If the operation fails, 
the function returns <b>NULL</b>. For more information, call the function  <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The  <b>ResUtilGetSzValue</b> utility function allocates the necessary memory for the string parameter value before calling the  <a href="/previous-versions/windows/desktop/mscs/cluster-api">Cluster API</a> function  <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregqueryvalue">ClusterRegQueryValue</a> to access the  <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a>. When you are finished with this memory, you must call the function  <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> to release it.

<b>ResUtilGetSzValue</b> also supports expandable and multiple string formats.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregqueryvalue">ClusterRegQueryValue</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetbinaryvalue">ResUtilGetBinaryValue</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetdwordvalue">ResUtilGetDwordValue</a>



[ResUtilGetExpandSzValue](./nf-resapi-resutilgetexpandszvalue.md)



<a href="/previous-versions/windows/desktop/api/resapi/nf-resapi-resutilgetmultiszvalue">ResUtilGetMultiSzValue</a>