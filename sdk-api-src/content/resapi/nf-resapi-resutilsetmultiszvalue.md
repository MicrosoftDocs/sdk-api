---
UID: NF:resapi.ResUtilSetMultiSzValue
title: ResUtilSetMultiSzValue function (resapi.h)
description: Sets a multiple string value in the cluster database. The PRESUTIL_SET_MULTI_SZ_VALUE type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_SET_MULTI_SZ_VALUE","PRESUTIL_SET_MULTI_SZ_VALUE function [Failover Cluster]","ResUtilSetMultiSzValue","ResUtilSetMultiSzValue function [Failover Cluster]","_wolf_resutilsetmultiszvalue","mscs.resutilsetmultiszvalue","resapi/PRESUTIL_SET_MULTI_SZ_VALUE","resapi/ResUtilSetMultiSzValue"]
old-location: mscs\resutilsetmultiszvalue.htm
tech.root: MsCS
ms.assetid: db048ce5-ca83-424b-853f-eda445176c0b
ms.date: 12/05/2018
ms.keywords: PRESUTIL_SET_MULTI_SZ_VALUE, PRESUTIL_SET_MULTI_SZ_VALUE function [Failover Cluster], ResUtilSetMultiSzValue, ResUtilSetMultiSzValue function [Failover Cluster], _wolf_resutilsetmultiszvalue, mscs.resutilsetmultiszvalue, resapi/PRESUTIL_SET_MULTI_SZ_VALUE, resapi/ResUtilSetMultiSzValue
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
 - ResUtilSetMultiSzValue
 - resapi/ResUtilSetMultiSzValue
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
 - ResUtilSetMultiSzValue
---

# ResUtilSetMultiSzValue function


## -description

Sets a multiple string value in the  <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a>. The <b>PRESUTIL_SET_MULTI_SZ_VALUE</b> type defines a pointer to this function.

## -parameters

### -param hkeyClusterKey [in]

Key identifying the location of the multiple string value in the cluster database.

### -param pszValueName [in]

Null-terminated Unicode string containing the name of the value to update.

### -param pszNewValue [in]

Pointer to the new multiple string value.

### -param cbNewValueSize [in]

Size of the new value.

### -param ppszOutValue [out, optional]

Pointer to a string pointer that receives a copy of the updated value. If used, callers must call <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> on *<i>ppszOutValue</i>.

### -param pcbOutValueSize [in, out, optional]

Pointer that receives the size of the new value.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

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
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
An error occurred while attempting to allocate memory.

</td>
</tr>
</table>

## -remarks

The  <b>ResUtilSetMultiSzValue</b> utility function allocates memory for the new value and calls the  <a href="/previous-versions/windows/desktop/mscs/cluster-api">Cluster API</a> function  <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregsetvalue">ClusterRegSetValue</a>.

A multiple string value is a large string containing smaller, contiguous, null-terminated Unicode strings and ending with an extra null character after the last string.

Be sure to call <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> on *<i>ppszOutValue</i> to avoid memory leaks.

Do not call  <b>ResUtilSetMultiSzValue</b> from the following resource DLL entry point functions:

<ul>
<li>
<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pclose_routine">Close</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-poffline_routine">Offline</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-ponline_routine">Online</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-popen_routine">Open</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pterminate_routine">Terminate</a>
</li>
</ul>
<b>ResUtilSetMultiSzValue</b> can be safely called from any other resource DLL entry point function or from a worker thread. For more information, see  <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregsetvalue">ClusterRegSetValue</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilsetbinaryvalue">ResUtilSetBinaryValue</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilsetdwordvalue">ResUtilSetDwordValue</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilsetexpandszvalue">ResUtilSetExpandSzValue</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilsetszvalue">ResUtilSetSzValue</a>