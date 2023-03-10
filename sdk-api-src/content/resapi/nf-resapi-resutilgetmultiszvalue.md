---
UID: NF:resapi.ResUtilGetMultiSzValue
title: ResUtilGetMultiSzValue function (resapi.h)
description: Returns a multiple string value from the cluster database.
helpviewer_keywords: ["ResUtilGetMultiSzValue","ResUtilGetMultiSzValue function [Failover Cluster]","_wolf_resutilgetmultiszvalue","mscs.resutilgetmultiszvalue","resapi/ResUtilGetMultiSzValue"]
old-location: mscs\resutilgetmultiszvalue.htm
tech.root: MsCS
ms.assetid: 09547806-16f4-40ce-8713-591a7691a588
ms.date: 12/05/2018
ms.keywords: ResUtilGetMultiSzValue, ResUtilGetMultiSzValue function [Failover Cluster], _wolf_resutilgetmultiszvalue, mscs.resutilgetmultiszvalue, resapi/ResUtilGetMultiSzValue
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ResUtilGetMultiSzValue
 - resapi/ResUtilGetMultiSzValue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ResApi.h
api_name:
 - ResUtilGetMultiSzValue
---

# ResUtilGetMultiSzValue function


## -description

Returns a multiple string value 
    from the <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a>.

## -parameters

### -param hkeyClusterKey [in]

Key identifying the location of the multiple string value in the cluster database.

### -param pszValueName [in]

Pointer to a null-terminated Unicode string containing the name of the value to retrieve.

### -param ppszOutValue [out, optional]

Address of the pointer to the retrieved value.

### -param pcbOutValueSize [out]

Pointer to a <b>DWORD</b> in which the size in bytes of the buffer pointed to by 
      <i>ppszOutValue</i> is returned.

## -returns

If the operations succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
       <a href="/windows/desktop/Debug/system-error-codes">system error code</a>. The following is a possible error 
       code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
An error occurred during memory allocation.

</td>
</tr>
</table>

## -remarks

When you are finished with the memory allocated for the value returned by the 
    <b>ResUtilGetMultiSzValue</b> utility function, you must call the function 
    <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> to release it.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregqueryvalue">ClusterRegQueryValue</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetbinaryvalue">ResUtilGetBinaryValue</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetdwordvalue">ResUtilGetDwordValue</a>



[ResUtilGetExpandSzValue](./nf-resapi-resutilgetexpandszvalue.md)



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetszvalue">ResUtilGetSzValue</a>