---
UID: NF:clusapi.ClusterRegDeleteValue
title: ClusterRegDeleteValue function (clusapi.h)
description: Removes a named value from a cluster database key.
helpviewer_keywords: ["ClusterRegDeleteValue","ClusterRegDeleteValue function [Failover Cluster]","_wolf_clusterregdeletevalue","clusapi/ClusterRegDeleteValue","mscs.clusterregdeletevalue"]
old-location: mscs\clusterregdeletevalue.htm
tech.root: MsCS
ms.assetid: 81d2936e-6f2c-48d9-b898-c1d8b2c946e6
ms.date: 12/05/2018
ms.keywords: ClusterRegDeleteValue, ClusterRegDeleteValue function [Failover Cluster], _wolf_clusterregdeletevalue, clusapi/ClusterRegDeleteValue, mscs.clusterregdeletevalue
req.header: clusapi.h
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
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ClusterRegDeleteValue
 - clusapi/ClusterRegDeleteValue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-cluster-clusapi-l1-1-6.dll
 - ext-ms-win-cluster-clusapi-l1-1-5.dll
 - ext-ms-win-cluster-clusapi-l1-1-4.dll
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
 - ext-ms-win-cluster-clusapi-l1-1-3.dll
api_name:
 - ClusterRegDeleteValue
---

# ClusterRegDeleteValue function


## -description

Removes a 
    named value from a <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a> key.

## -parameters

### -param hKey [in]

Handle to a currently open key.

### -param lpszValueName [in]

Pointer to a null-terminated Unicode string containing the name of the value to be removed.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
       <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -remarks

Do not call <b>ClusterRegDeleteValue</b> from the 
     following resource DLL entry point functions:

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
<b>ClusterRegDeleteValue</b> can be safely called 
     from any other resource DLL entry point function or from a worker thread. For more information, see 
     <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregopenkey">ClusterRegOpenKey</a>