---
UID: NF:resapi.ResUtilSetBinaryValue
title: ResUtilSetBinaryValue function (resapi.h)
description: Sets a binary value in the cluster database.
helpviewer_keywords: ["PRESUTIL_SET_BINARY_VALUE","PRESUTIL_SET_BINARY_VALUE function [Failover Cluster]","ResUtilSetBinaryValue","ResUtilSetBinaryValue function [Failover Cluster]","_wolf_resutilsetbinaryvalue","mscs.resutilsetbinaryvalue","resapi/PRESUTIL_SET_BINARY_VALUE","resapi/ResUtilSetBinaryValue"]
old-location: mscs\resutilsetbinaryvalue.htm
tech.root: MsCS
ms.assetid: 6a32169c-af14-40f4-ac45-f9923da544ca
ms.date: 12/05/2018
ms.keywords: PRESUTIL_SET_BINARY_VALUE, PRESUTIL_SET_BINARY_VALUE function [Failover Cluster], ResUtilSetBinaryValue, ResUtilSetBinaryValue function [Failover Cluster], _wolf_resutilsetbinaryvalue, mscs.resutilsetbinaryvalue, resapi/PRESUTIL_SET_BINARY_VALUE, resapi/ResUtilSetBinaryValue
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
 - ResUtilSetBinaryValue
 - resapi/ResUtilSetBinaryValue
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
 - ResUtilSetBinaryValue
---

# ResUtilSetBinaryValue function


## -description

Sets a binary value in the  <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a>.

## -parameters

### -param hkeyClusterKey [in]

Key identifying the location of the binary value in the cluster database.

### -param pszValueName [in]

A null-terminated Unicode string containing the name of the value to update.

### -param pbNewValue [in]

Pointer to the new binary value.

### -param cbNewValueSize [in]

Size of the new binary value.

### -param ppbOutValue [in, out, optional]

Address of a pointer to the new binary value.

### -param pcbOutValueSize [in, out]

Pointer to a <b>DWORD</b> in which the size in bytes of the value pointed to by <i>ppbOutValue</i> is returned.

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
An error occurred during memory allocation.

</td>
</tr>
</table>

## -remarks

The  <b>ResUtilSetBinaryValue</b> utility function allocates memory for the <i>ppbOutValue</i> pointer using the function  <a href="/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a>, calls the  <a href="/previous-versions/windows/desktop/mscs/cluster-api">Cluster API</a> function  <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregsetvalue">ClusterRegSetValue</a>, and then copies the new value to this buffer. If the pointer is not <b>NULL</b>,  <b>ResUtilSetBinaryValue</b> also deallocates it. As callers of this function, you are responsible for deallocating the buffer using the function  <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a>.

Do not call  <b>ResUtilSetBinaryValue</b> from the following resource DLL entry point functions:

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
<b>ResUtilSetBinaryValue</b> can be safely called from any other resource DLL entry point function or from a worker thread. For more information, see  <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregsetvalue">ClusterRegSetValue</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilsetdwordvalue">ResUtilSetDwordValue</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilsetexpandszvalue">ResUtilSetExpandSzValue</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilsetmultiszvalue">ResUtilSetMultiSzValue</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilsetszvalue">ResUtilSetSzValue</a>