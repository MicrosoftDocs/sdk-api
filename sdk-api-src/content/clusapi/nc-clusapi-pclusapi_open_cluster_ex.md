---
UID: NC:clusapi.PCLUSAPI_OPEN_CLUSTER_EX
title: PCLUSAPI_OPEN_CLUSTER_EX
author: windows-driver-content
description: Opens a connection to a cluster and returns a handle to it.
old-location: mscs\openclusterex.htm
old-project: MsCS
ms.assetid: 688702b7-7525-48d6-9e44-d7c4969565f8
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: PCLUSAPI_OPEN_CLUSTER_EX, PCLUSAPI_OPEN_CLUSTER_EX callback, PCLUSAPI_OPEN_CLUSTER_EX callback function [Failover Cluster], clusapi/PCLUSAPI_OPEN_CLUSTER_EX, mscs.openclusterex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 Datacenter, Windows Server 2008 R2 Enterprise
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: Sources
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ClusAPI.h
api_name:
-	PCLUSAPI_OPEN_CLUSTER_EX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_OPEN_CLUSTER_EX callback function


## -description


Opens a connection to a 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a> and returns a handle to it.


## -parameters




### -param lpszClusterName [in, optional]

Specifies one of the following values:

<ul>
<li>Pointer to a null-terminated Unicode string containing the name of the cluster or one of the cluster 
        <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">nodes</a> expressed as a NetBIOS name, a fully qualified DNS name, or 
        an IP address. This produces an RPC cluster handle.</li>
<li><b>NULL</b>, which produces an LPC handle to the cluster to which the local computer 
        belongs.</li>
</ul>

### -param dwDesiredAccess


### -param lpdwGrantedAccess








#### - DesiredAccess [in]

The requested access privileges. This may be any combination of <b>GENERIC_READ</b> 
      (0x80000000), <b>GENERIC_ALL</b> (0x10000000), or <b>MAXIMUM_ALLOWED</b> 
      (0x02000000). If this value is zero (0) and undefined error may be returned. Using 
      <b>GENERIC_ALL</b> is the same as calling 
      <a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>.


#### - GrantedAccess [out, optional]

Optional parameter that contains the address of a <b>DWORD</b> that will receive the 
      access rights granted. If the <i>DesiredAccess</i> parameter is 
      <b>MAXIMUM_ALLOWED</b> (0x02000000) then the <b>DWORD</b> pointed to by 
      this parameter will contain the maximum privileges granted to this user.


## -returns



If the operation was successful, <i>OpenClusterEx</i> returns 
       a cluster handle.




## -remarks



A cluster handle is a pointer to an internally defined structure which stores information about the RPC or LPC 
     connection to the cluster. Any object handles obtained from the cluster handle will be associated with the RPC or 
     LPC session data stored in the cluster structure. Combining RPC and LPC handles or using handles obtained from 
     different contexts can cause exceptions or other unpredictable results. For more information, see 
     <a href="https://msdn.microsoft.com/0fdb2024-9b04-4a38-baf9-3cdabba9bf8c">LPC and RPC Handles</a>.

When finished with a cluster handle, it is important to call 
     <a href="https://msdn.microsoft.com/cf055fd6-b1e1-4262-b205-c7d926522450">CloseCluster</a> to ensure that all memory is freed and the 
     connection is shut down cleanly.



