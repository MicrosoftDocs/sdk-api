---
UID: NF:resapi.ResUtilSetExpandSzValue
title: ResUtilSetExpandSzValue function (resapi.h)
description: Sets an expandable string value in the cluster database. The PRESUTIL_SET_EXPAND_SZ_VALUE type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_SET_EXPAND_SZ_VALUE","PRESUTIL_SET_EXPAND_SZ_VALUE function [Failover Cluster]","ResUtilSetExpandSzValue","ResUtilSetExpandSzValue function [Failover Cluster]","_wolf_resutilsetexpandszvalue","mscs.resutilsetexpandszvalue","resapi/PRESUTIL_SET_EXPAND_SZ_VALUE","resapi/ResUtilSetExpandSzValue"]
old-location: mscs\resutilsetexpandszvalue.htm
tech.root: MsCS
ms.assetid: a2049be4-cebb-45bf-b2f7-40841e379b12
ms.date: 12/05/2018
ms.keywords: PRESUTIL_SET_EXPAND_SZ_VALUE, PRESUTIL_SET_EXPAND_SZ_VALUE function [Failover Cluster], ResUtilSetExpandSzValue, ResUtilSetExpandSzValue function [Failover Cluster], _wolf_resutilsetexpandszvalue, mscs.resutilsetexpandszvalue, resapi/PRESUTIL_SET_EXPAND_SZ_VALUE, resapi/ResUtilSetExpandSzValue
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
 - ResUtilSetExpandSzValue
 - resapi/ResUtilSetExpandSzValue
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
 - ResUtilSetExpandSzValue
---

# ResUtilSetExpandSzValue function


## -description

Sets an <a href="/previous-versions/windows/desktop/mscs/e-gly">expandable string</a> value in the  <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a>. The <b>PRESUTIL_SET_EXPAND_SZ_VALUE</b> type defines a pointer to this function.

## -parameters

### -param hkeyClusterKey [in]

Key identifying the location of the expandable string value in the cluster database.

### -param pszValueName [in]

null-terminated Unicode string containing the name of the value to update.

### -param pszNewValue [in]

Pointer to the new expandable string value.

### -param ppszOutString [in, out, optional]

Pointer to a string pointer that receives a copy of the updated value. If used, callers must call <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> on *<i>ppszOutValue</i>.

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

The  <b>ResUtilSetExpandSzValue</b> utility function allocates memory for the new value and calls the  <a href="/previous-versions/windows/desktop/mscs/cluster-api">Cluster API</a> function  <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregsetvalue">ClusterRegSetValue</a>.

An expandable string value contains data that represents a null-terminated Unicode string containing unexpanded references to environment variables such as "%SystemRoot%".

Be sure to call <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> on *<i>ppszOutValue</i> to avoid memory leaks.

Do not call  <b>ResUtilSetExpandSzValue</b> from the following resource DLL entry point functions:

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
<b>ResUtilSetExpandSzValue</b> can be safely called from any other resource DLL entry point function or from a worker thread. For more information, see  <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregsetvalue">ClusterRegSetValue</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilsetbinaryvalue">ResUtilSetBinaryValue</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilsetdwordvalue">ResUtilSetDwordValue</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilsetmultiszvalue">ResUtilSetMultiSzValue</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilsetszvalue">ResUtilSetSzValue</a>