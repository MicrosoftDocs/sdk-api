---
UID: NF:clusapi.ClusterRegSetKeySecurity
title: ClusterRegSetKeySecurity function
author: windows-sdk-content
description: Sets the security attributes for a cluster database key.
old-location: mscs\clusterregsetkeysecurity.htm
old-project: MsCS
ms.assetid: adb2ea52-6a3a-4243-944d-c7ae68a42a1a
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: ClusterRegSetKeySecurity, ClusterRegSetKeySecurity function [Failover Cluster], _wolf_clusterregsetkeysecurity, clusapi/ClusterRegSetKeySecurity, mscs.clusterregsetkeysecurity
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: SR_REPLICATED_DISK_TYPE, *PSR_REPLICATED_DISK_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	ClusAPI.dll
api_name:
-	ClusterRegSetKeySecurity
product: Windows
targetos: Windows
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
---

# ClusterRegSetKeySecurity function


## -description


Sets the security attributes for a <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a> 
    key.


## -parameters




### -param hKey [in]

Handle to a cluster database key.


### -param SecurityInformation [in]

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff556635">SECURITY_INFORMATION</a> structure that 
       indicates the content of the security descriptor pointed to by 
       <i>pSecurityDescriptor</i>.


### -param pSecurityDescriptor [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a> structure 
       that describes the security attributes to set for the key corresponding to <i>hKey</i>.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b> (0).

If the operation fails, the function returns a 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -remarks



The <b>ClusterRegSetKeySecurity</b> function 
     generates a <b>CLUSTER_CHANGE_REGISTRY_ATTRIBUTES</b> event for all registered notification 
     ports.

Do not call <b>ClusterRegSetKeySecurity</b> from 
     the following resource DLL entry point functions:

<ul>
<li>
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a>
</li>
<li>
<a href="https://msdn.microsoft.com/library/windows/hardware/dn997350">Offline</a>
</li>
<li>
<a href="https://msdn.microsoft.com/library/windows/hardware/dn997353">Online</a>
</li>
<li>
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b53ab7db-ed17-4386-8a5f-5d0b0d1cb1b3">Terminate</a>
</li>
</ul>
<b>ClusterRegSetKeySecurity</b> can be safely 
     called from any other resource DLL entry point function or from a worker thread. For more information, see 
     <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/f2cf204e-d02d-40b9-86d7-0262b8cc4db1">ClusterRegOpenKey</a>
 

 

