---
UID: NF:clusapi.ClusterRegSetKeySecurity
title: ClusterRegSetKeySecurity function
author: windows-sdk-content
description: Sets the security attributes for a cluster database key.
old-location: mscs\clusterregsetkeysecurity.htm
tech.root: mscs
ms.assetid: adb2ea52-6a3a-4243-944d-c7ae68a42a1a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ClusterRegSetKeySecurity, ClusterRegSetKeySecurity function [Failover Cluster], _wolf_clusterregsetkeysecurity, clusapi/ClusterRegSetKeySecurity, mscs.clusterregsetkeysecurity
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
api_name:
 - ClusterRegSetKeySecurity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterRegSetKeySecurity function


## -description


Sets the security attributes for a <a href="https://msdn.microsoft.com/en-us/library/Aa369094(v=VS.85).aspx">cluster database</a> 
    key.


## -parameters




### -param hKey [in]

Handle to a cluster database key.


### -param SecurityInformation [in]

A <a href="https://msdn.microsoft.com/en-us/library/Aa379573(v=VS.85).aspx">SECURITY_INFORMATION</a> structure that 
       indicates the content of the security descriptor pointed to by 
       <i>pSecurityDescriptor</i>.


### -param pSecurityDescriptor [in]

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Aa379561(v=VS.85).aspx">SECURITY_DESCRIPTOR</a> structure 
       that describes the security attributes to set for the key corresponding to <i>hKey</i>.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b> (0).

If the operation fails, the function returns a 
       <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error code</a>.




## -remarks



The <b>ClusterRegSetKeySecurity</b> function 
     generates a <b>CLUSTER_CHANGE_REGISTRY_ATTRIBUTES</b> event for all registered notification 
     ports.

Do not call <b>ClusterRegSetKeySecurity</b> from 
     the following resource DLL entry point functions:

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367196(v=VS.85).aspx">Close</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa371767(v=VS.85).aspx">Offline</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa371770(v=VS.85).aspx">Online</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa371773(v=VS.85).aspx">Open</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa372939(v=VS.85).aspx">Terminate</a>
</li>
</ul>
<b>ClusterRegSetKeySecurity</b> can be safely 
     called from any other resource DLL entry point function or from a worker thread. For more information, see 
     <a href="https://msdn.microsoft.com/en-us/library/Aa369588(v=VS.85).aspx">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa369004(v=VS.85).aspx">ClusterRegOpenKey</a>
 

 

