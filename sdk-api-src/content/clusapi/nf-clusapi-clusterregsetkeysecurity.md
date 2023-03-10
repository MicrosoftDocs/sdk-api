---
UID: NF:clusapi.ClusterRegSetKeySecurity
title: ClusterRegSetKeySecurity function (clusapi.h)
description: Sets the security attributes for a cluster database key.
helpviewer_keywords: ["ClusterRegSetKeySecurity","ClusterRegSetKeySecurity function [Failover Cluster]","_wolf_clusterregsetkeysecurity","clusapi/ClusterRegSetKeySecurity","mscs.clusterregsetkeysecurity"]
old-location: mscs\clusterregsetkeysecurity.htm
tech.root: MsCS
ms.assetid: adb2ea52-6a3a-4243-944d-c7ae68a42a1a
ms.date: 12/05/2018
ms.keywords: ClusterRegSetKeySecurity, ClusterRegSetKeySecurity function [Failover Cluster], _wolf_clusterregsetkeysecurity, clusapi/ClusterRegSetKeySecurity, mscs.clusterregsetkeysecurity
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
 - ClusterRegSetKeySecurity
 - clusapi/ClusterRegSetKeySecurity
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
api_name:
 - ClusterRegSetKeySecurity
---

# ClusterRegSetKeySecurity function


## -description

Sets the security attributes for a <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a> 
    key.

## -parameters

### -param hKey [in]

Handle to a cluster database key.

### -param SecurityInformation [in]

A <a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a> structure that 
       indicates the content of the security descriptor pointed to by 
       <i>pSecurityDescriptor</i>.

### -param pSecurityDescriptor [in]

Pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure 
       that describes the security attributes to set for the key corresponding to <i>hKey</i>.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b> (0).

If the operation fails, the function returns a 
       <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -remarks

The <b>ClusterRegSetKeySecurity</b> function 
     generates a <b>CLUSTER_CHANGE_REGISTRY_ATTRIBUTES</b> event for all registered notification 
     ports.

Do not call <b>ClusterRegSetKeySecurity</b> from 
     the following resource DLL entry point functions:

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
<b>ClusterRegSetKeySecurity</b> can be safely 
     called from any other resource DLL entry point function or from a worker thread. For more information, see 
     <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregopenkey">ClusterRegOpenKey</a>