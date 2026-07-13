---
UID: NF:resapi.ResUtilSetSzValue
title: ResUtilSetSzValue function (resapi.h)
description: Sets a string value in the cluster database. The PRESUTIL_SET_SZ_VALUE type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_SET_SZ_VALUE","PRESUTIL_SET_SZ_VALUE function [Failover Cluster]","ResUtilSetSzValue","ResUtilSetSzValue function [Failover Cluster]","_wolf_resutilsetszvalue","mscs.resutilsetszvalue","resapi/PRESUTIL_SET_SZ_VALUE","resapi/ResUtilSetSzValue"]
old-location: mscs\resutilsetszvalue.htm
tech.root: MsCS
ms.assetid: b9227df3-0693-4b0f-99de-d10fa3d7acf5
ms.date: 12/05/2018
ms.keywords: PRESUTIL_SET_SZ_VALUE, PRESUTIL_SET_SZ_VALUE function [Failover Cluster], ResUtilSetSzValue, ResUtilSetSzValue function [Failover Cluster], _wolf_resutilsetszvalue, mscs.resutilsetszvalue, resapi/PRESUTIL_SET_SZ_VALUE, resapi/ResUtilSetSzValue
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
 - ResUtilSetSzValue
 - resapi/ResUtilSetSzValue
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
 - ResUtilSetSzValue
---

# ResUtilSetSzValue function


## -description

Sets a string value in the  <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a>. The <b>PRESUTIL_SET_SZ_VALUE</b> type defines a pointer to this function.

## -parameters

### -param hkeyClusterKey [in]

Key identifying the location of the string value in the cluster database.

### -param pszValueName [in]

Null-terminated Unicode string containing the name of the value to update.

### -param pszNewValue [in]

Pointer to the new string value.

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

The  <b>ResUtilSetSzValue</b> utility function allocates memory for the new value and calls the  <a href="/previous-versions/windows/desktop/mscs/cluster-api">Cluster API</a> function  <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregsetvalue">ClusterRegSetValue</a>. If necessary, a previous value is deallocated. The new value is copied to the content of <i>ppszOutValue</i>.

Be sure to call <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> on *<i>ppszOutValue</i> to avoid memory leaks.

Do not call  <b>ResUtilSetSzValue</b> from the following resource DLL entry point functions:

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
<b>ResUtilSetSzValue</b> can be safely called from any other resource DLL entry point function or from a worker thread. For more information, see  <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregsetvalue">ClusterRegSetValue</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilsetbinaryvalue">ResUtilSetBinaryValue</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilsetdwordvalue">ResUtilSetDwordValue</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilsetexpandszvalue">ResUtilSetExpandSzValue</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilsetmultiszvalue">ResUtilSetMultiSzValue</a>