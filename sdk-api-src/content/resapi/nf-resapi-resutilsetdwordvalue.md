---
UID: NF:resapi.ResUtilSetDwordValue
title: ResUtilSetDwordValue function (resapi.h)
description: Sets a numeric value in the cluster database. The PRESUTIL_SET_DWORD_VALUE type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_SET_DWORD_VALUE","PRESUTIL_SET_DWORD_VALUE function [Failover Cluster]","ResUtilSetDwordValue","ResUtilSetDwordValue function [Failover Cluster]","_wolf_resutilsetdwordvalue","mscs.resutilsetdwordvalue","resapi/PRESUTIL_SET_DWORD_VALUE","resapi/ResUtilSetDwordValue"]
old-location: mscs\resutilsetdwordvalue.htm
tech.root: MsCS
ms.assetid: e8b4393b-84f7-4440-92b5-fd7fa2be96a2
ms.date: 12/05/2018
ms.keywords: PRESUTIL_SET_DWORD_VALUE, PRESUTIL_SET_DWORD_VALUE function [Failover Cluster], ResUtilSetDwordValue, ResUtilSetDwordValue function [Failover Cluster], _wolf_resutilsetdwordvalue, mscs.resutilsetdwordvalue, resapi/PRESUTIL_SET_DWORD_VALUE, resapi/ResUtilSetDwordValue
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
 - ResUtilSetDwordValue
 - resapi/ResUtilSetDwordValue
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
 - ResUtilSetDwordValue
---

# ResUtilSetDwordValue function


## -description

Sets a numeric value in the  <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a>. The <b>PRESUTIL_SET_DWORD_VALUE</b> type defines a pointer to this function.

## -parameters

### -param hkeyClusterKey [in]

Key identifying the location of the numeric value in the cluster database.

### -param pszValueName [in]

A null-terminated Unicode string containing the name of the value to update.

### -param dwNewValue [in]

New <b>DWORD</b> value.

### -param pdwOutValue [in, out]

Optional. Pointer to where the updated value should be copied.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -remarks

The  <b>ResUtilSetDwordValue</b> utility function updates the cluster database by calling the  <a href="/previous-versions/windows/desktop/mscs/cluster-api">Cluster API</a> function  <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregsetvalue">ClusterRegSetValue</a>.

Do not call  <b>ResUtilSetDwordValue</b> from the following resource DLL entry point functions:

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
<b>ResUtilSetDwordValue</b> can be safely called from any other resource DLL entry point function or from a worker thread. For more information, see  <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregsetvalue">ClusterRegSetValue</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilsetbinaryvalue">ResUtilSetBinaryValue</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilsetexpandszvalue">ResUtilSetExpandSzValue</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilsetmultiszvalue">ResUtilSetMultiSzValue</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilsetszvalue">ResUtilSetSzValue</a>