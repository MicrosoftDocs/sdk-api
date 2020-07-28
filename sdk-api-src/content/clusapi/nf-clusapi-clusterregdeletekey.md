---
UID: NF:clusapi.ClusterRegDeleteKey
title: ClusterRegDeleteKey function (clusapi.h)
description: Deletes a cluster database key.
helpviewer_keywords: ["ClusterRegDeleteKey","ClusterRegDeleteKey function [Failover Cluster]","_wolf_clusterregdeletekey","clusapi/ClusterRegDeleteKey","mscs.clusterregdeletekey"]
old-location: mscs\clusterregdeletekey.htm
tech.root: MsCS
ms.assetid: af2b3b9c-2ff1-483e-a9cf-5db7b1fcbd85
ms.date: 12/05/2018
ms.keywords: ClusterRegDeleteKey, ClusterRegDeleteKey function [Failover Cluster], _wolf_clusterregdeletekey, clusapi/ClusterRegDeleteKey, mscs.clusterregdeletekey
f1_keywords:
- clusapi/ClusterRegDeleteKey
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- ClusAPI.dll
- Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
- Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
- ext-ms-win-cluster-clusapi-l1-1-3.dll
api_name:
- ClusterRegDeleteKey
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ClusterRegDeleteKey function


## -description


Deletes a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a> key.


## -parameters




### -param hKey [in]

Handle to a currently open key.


### -param lpszSubKey [in]

Pointer to a null-terminated Unicode string specifying the name of the key to delete. The key pointed to by 
      <i>lpszSubKey</i> cannot have subkeys; 
      <b>ClusterRegDeleteKey</b> can only delete keys without 
      subkeys. This parameter cannot be <b>NULL</b>.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b> (0).

If the operation fails, the function returns a 
       <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error code</a>.




## -remarks



The <b>ClusterRegDeleteKey</b> function cannot delete 
    a key that has one or more subkeys.

Do not call <b>ClusterRegDeleteKey</b> from the 
    following resource DLL entry point functions:

<ul>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/resapi/nc-resapi-pclose_routine">Close</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/resapi/nc-resapi-poffline_routine">Offline</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/resapi/nc-resapi-ponline_routine">Online</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/resapi/nc-resapi-popen_routine">Open</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/resapi/nc-resapi-pterminate_routine">Terminate</a>
</li>
</ul>
<b>ClusterRegDeleteKey</b> can be safely called from 
    any other resource DLL entry point function or from a worker thread. For more information, see 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregcreatekey">ClusterRegCreateKey</a>
 

 

