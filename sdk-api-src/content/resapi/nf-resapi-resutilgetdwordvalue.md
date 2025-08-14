---
UID: NF:resapi.ResUtilGetDwordValue
title: ResUtilGetDwordValue function (resapi.h)
description: Returns a numeric value from the cluster database.
helpviewer_keywords: ["PRESUTIL_GET_DWORD_VALUE","PRESUTIL_GET_DWORD_VALUE function [Failover Cluster]","ResUtilGetDwordValue","ResUtilGetDwordValue function [Failover Cluster]","_wolf_resutilgetdwordvalue","mscs.resutilgetdwordvalue","resapi/PRESUTIL_GET_DWORD_VALUE","resapi/ResUtilGetDwordValue"]
old-location: mscs\resutilgetdwordvalue.htm
tech.root: MsCS
ms.assetid: 2db6126e-a3a7-415b-a436-c3d0748fbc65
ms.date: 12/05/2018
ms.keywords: PRESUTIL_GET_DWORD_VALUE, PRESUTIL_GET_DWORD_VALUE function [Failover Cluster], ResUtilGetDwordValue, ResUtilGetDwordValue function [Failover Cluster], _wolf_resutilgetdwordvalue, mscs.resutilgetdwordvalue, resapi/PRESUTIL_GET_DWORD_VALUE, resapi/ResUtilGetDwordValue
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
 - ResUtilGetDwordValue
 - resapi/ResUtilGetDwordValue
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
 - ResUtilGetDwordValue
---

# ResUtilGetDwordValue function


## -description

Returns a numeric value from the  <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a>.

## -parameters

### -param hkeyClusterKey [in]

Key identifying the location of the numeric value in the cluster database.

### -param pszValueName [in]

Pointer to a null-terminated Unicode string containing the name of the value to retrieve.

### -param pdwOutValue [out]

Pointer to the retrieved value.

### -param dwDefaultValue [in]

Value to return if the value pointed to by <i>pszValueName</i> is not found.

## -returns

If the operations succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>. The following is a possible error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The value pointed to by <i>ValueName</i> is not a numeric value.

</td>
</tr>
</table>

## -remarks

The  <b>ResUtilGetDwordValue</b> utility function calls the  <a href="/previous-versions/windows/desktop/mscs/cluster-api">Cluster API</a> function  <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregqueryvalue">ClusterRegQueryValue</a> to retrieve the value.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregqueryvalue">ClusterRegQueryValue</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetbinaryvalue">ResUtilGetBinaryValue</a>



[ResUtilGetExpandSzValue](./nf-resapi-resutilgetexpandszvalue.md)



<a href="/previous-versions/windows/desktop/api/resapi/nf-resapi-resutilgetmultiszvalue">ResUtilGetMultiSzValue</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetszvalue">ResUtilGetSzValue</a>