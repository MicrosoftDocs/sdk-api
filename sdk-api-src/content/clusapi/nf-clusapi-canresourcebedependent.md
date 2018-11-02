---
UID: NF:clusapi.CanResourceBeDependent
title: CanResourceBeDependent function
author: windows-sdk-content
description: Determines if one resource can be dependent upon another resource.
old-location: mscs\canresourcebedependent.htm
tech.root: mscs
ms.assetid: 974ec036-3dd3-4453-9ce5-029f58d99d81
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: CanResourceBeDependent, CanResourceBeDependent function [Failover Cluster], PCLUSAPI_CAN_RESOURCE_BE_DEPENDENT, PCLUSAPI_CAN_RESOURCE_BE_DEPENDENT function [Failover Cluster], _wolf_canresourcebedependent, clusapi/CanResourceBeDependent, clusapi/PCLUSAPI_CAN_RESOURCE_BE_DEPENDENT, mscs.canresourcebedependent
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
 - Ext-MS-Win-Cluster-ClusAPI-L1-1-2.dll
api_name:
 - CanResourceBeDependent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CanResourceBeDependent function


## -description


Determines if one  <a href="https://msdn.microsoft.com/en-us/library/Aa372152(v=VS.85).aspx">resource</a> can be  <a href="https://msdn.microsoft.com/en-us/library/Aa372236(v=VS.85).aspx">dependent</a> upon another resource. The <b>PCLUSAPI_CAN_RESOURCE_BE_DEPENDENT</b> type defines a pointer to this function.


## -parameters




### -param hResource [in]

Handle to the resource in question.


### -param hResourceDependent [in]

Handle to the resource upon which the resource identified by <i>hResource</i> may depend.


## -returns



This function returns BOOL.




## -remarks



With the  <b>CanResourceBeDependent</b> function, for the resource identified by <i>hResource</i> to be dependent on the resource identified by <i>hResourceDependent</i>, the following must be true:

<ul>
<li>Both resources must be members of the same  <a href="https://msdn.microsoft.com/en-us/library/Aa369645(v=VS.85).aspx">group</a>.</li>
<li>The resource identified by <i>hResourceDependent</i> cannot depend on the resource identified by <i>hResource</i>, either directly or indirectly.</li>
</ul>
Do not call  <b>CanResourceBeDependent</b> from any resource DLL entry point function.  <b>CanResourceBeDependent</b> can safely be called from a worker thread. For more information, see  <a href="https://msdn.microsoft.com/en-us/library/Aa369588(v=VS.85).aspx">Function Calls to Avoid in Resource DLLs</a>.

Do not pass LPC and RPC handles to the same function call. Otherwise, the call will raise an RPC exception and can have additional destructive effects. For information on how LPC and RPC handles are created, see  <a href="https://msdn.microsoft.com/en-us/library/Aa372959(v=VS.85).aspx">Using Object Handles</a> and  <a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>.




## -see-also




<a href="https://msdn.microsoft.com/37f173f3-514e-434b-8531-d308c6233a24">AddClusterResourceDependency</a>



<a href="https://msdn.microsoft.com/c699cb00-b999-45b8-b9db-570150e1a65e">OpenClusterResource</a>



<a href="https://msdn.microsoft.com/3640ad8d-db0d-4e55-bff0-35fb5d26776f">RemoveClusterResourceDependency</a>
 

 

