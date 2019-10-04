---
UID: NF:resapi.ResUtilGetSzValue
title: ResUtilGetSzValue function (resapi.h)
author: windows-sdk-content
description: Returns a string value from the cluster database.
old-location: mscs\resutilgetszvalue.htm
tech.root: MsCS
ms.assetid: c2ba04ea-0f98-4513-b8f8-658056a493e6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PRESUTIL_GET_SZ_VALUE, PRESUTIL_GET_SZ_VALUE function [Failover Cluster], ResUtilGetSzValue, ResUtilGetSzValue function [Failover Cluster], _wolf_resutilgetszvalue, mscs.resutilgetszvalue, resapi/PRESUTIL_GET_SZ_VALUE, resapi/ResUtilGetSzValue
ms.topic: function
f1_keywords: 
 - "resapi/ResUtilGetSzValue"
dev_langs:
 - c++
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
 - ResUtilGetSzValue
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ResUtilGetSzValue function


## -description


Returns a string value from the  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a>.


## -parameters




### -param hkeyClusterKey [in]

Key identifying the location of the value in the cluster database.


### -param pszValueName [in]

A null-terminated Unicode string containing the name of the value to retrieve.


## -returns



If the operation succeeds, 
the function returns a pointer to a buffer containing the string value.

If the operation fails, 
the function returns <b>NULL</b>. For more information, call the function  <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



The  <b>ResUtilGetSzValue</b> utility function allocates the necessary memory for the string parameter value before calling the  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluster-api">Cluster API</a> function  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregqueryvalue">ClusterRegQueryValue</a> to access the  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a>. When you are finished with this memory, you must call the function  <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> to release it.

<b>ResUtilGetSzValue</b> also supports expandable and multiple string formats.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregqueryvalue">ClusterRegQueryValue</a>



<a href="https://docs.microsoft.com/windows/desktop/api/resapi/nf-resapi-resutilgetbinaryvalue">ResUtilGetBinaryValue</a>



<a href="https://docs.microsoft.com/windows/desktop/api/resapi/nf-resapi-resutilgetdwordvalue">ResUtilGetDwordValue</a>



<a href="https://docs.microsoft.com/windows/desktop/api/resapi/nc-resapi-presutil_get_expand_sz_value">ResUtilGetExpandSzValue</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/resapi/nf-resapi-resutilgetmultiszvalue">ResUtilGetMultiSzValue</a>
 

 

