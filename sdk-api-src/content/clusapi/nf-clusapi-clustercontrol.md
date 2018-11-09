---
UID: NF:clusapi.ClusterControl
title: ClusterControl function
author: windows-sdk-content
description: Initiates an operation that affects a cluster.
old-location: mscs\clustercontrol.htm
tech.root: mscs
ms.assetid: 7ef06c95-8d9d-4b87-a6d8-d6a2d49523ee
ms.author: windowssdkdev
ms.date: 11/06/2018
ms.keywords: ClusterControl, ClusterControl function [Failover Cluster], _wolf_clustercontrol, clusapi/ClusterControl, mscs.clustercontrol
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
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - ClusterControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterControl function


## -description


Initiates an 
    operation that affects a <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster</a>. The operation 
    performed depends on the <a href="https://msdn.microsoft.com/en-us/library/Aa369307(v=VS.85).aspx">control code</a> passed to the 
    <i>dwControlCode</i> parameter.


## -parameters




### -param hCluster [in]

Handle to the cluster to be affected.


### -param hHostNode [in, optional]

If non-<b>NULL</b>, handle to the node to perform the operation represented by the control 
       code. If <b>NULL</b>, the local node performs the operation. Specifying 
       <i>hHostNode</i> is optional.


### -param dwControlCode [in]

A <a href="https://msdn.microsoft.com/en-us/library/Aa369093(v=VS.85).aspx">cluster control code</a> from the 
       <a href="https://msdn.microsoft.com/en-us/library/Cc307916(v=VS.85).aspx">CLUSCTL_CLUSTER_CODES</a> enumeration that specifies 
       the operation to be performed. For the syntax associated with a control code, refer to 
       <a href="https://msdn.microsoft.com/en-us/library/Aa369308(v=VS.85).aspx">Control Code Architecture</a> and the following 
       topics:


<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb309078(v=VS.85).aspx">CLUSCTL_CLUSTER_CHECK_VOTER_DOWN</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb309079(v=VS.85).aspx">CLUSCTL_CLUSTER_CHECK_VOTER_EVICT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Mt791986(v=VS.85).aspx">CLUSCTL_CLUSTER_CLEAR_NODE_CONNECTION_INFO</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367218(v=VS.85).aspx">CLUSCTL_CLUSTER_ENUM_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367219(v=VS.85).aspx">CLUSCTL_CLUSTER_ENUM_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367220(v=VS.85).aspx">CLUSCTL_CLUSTER_GET_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367223(v=VS.85).aspx">CLUSCTL_CLUSTER_GET_FQDN</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367221(v=VS.85).aspx">CLUSCTL_CLUSTER_GET_COMMON_PROPERTY_FMTS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367224(v=VS.85).aspx">CLUSCTL_CLUSTER_GET_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367225(v=VS.85).aspx">CLUSCTL_CLUSTER_GET_PRIVATE_PROPERTY_FMTS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367226(v=VS.85).aspx">CLUSCTL_CLUSTER_GET_RO_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367227(v=VS.85).aspx">CLUSCTL_CLUSTER_GET_RO_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Ee342490(v=VS.85).aspx">CLUSCTL_CLUSTER_GET_SHARED_VOLUME_ID</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367228(v=VS.85).aspx">CLUSCTL_CLUSTER_SET_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367229(v=VS.85).aspx">CLUSCTL_CLUSTER_SET_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb309080(v=VS.85).aspx">CLUSCTL_CLUSTER_SHUTDOWN</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367230(v=VS.85).aspx">CLUSCTL_CLUSTER_UNKNOWN</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367231(v=VS.85).aspx">CLUSCTL_CLUSTER_VALIDATE_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367232(v=VS.85).aspx">CLUSCTL_CLUSTER_VALIDATE_PRIVATE_PROPERTIES</a>
</li>
</ul>



### -param lpInBuffer [in, optional]

Pointer to an input buffer containing information needed for the operation, or <b>NULL</b> 
       if no information is needed.


### -param nInBufferSize [in]

The allocated size (in bytes) of the input buffer.


### -param lpOutBuffer [out, optional]

Pointer to an output buffer to receive the data resulting from the operation, or 
       <b>NULL</b> if no data will be returned.


### -param nOutBufferSize [in]

The allocated size (in bytes) of the output buffer.


### -param lpBytesReturned [out, optional]

Returns the actual size (in bytes) of the data resulting from the operation. If this information is not 
       needed, pass <b>NULL</b> for <i>lpcbBytesReturned</i>.


## -returns



The function returns one of the following values.




## -remarks



If <b>ClusterControl</b> returns 
     <b>ERROR_MORE_DATA</b>, set <i>nOutBufferSize</i> to the number of bytes 
     pointed to by <i>lpcbBytesReturned</i> and call the function again.

Do not pass LPC and RPC handles to the same function call. Otherwise, the call will raise an RPC exception and 
     can have additional destructive effects. For information on how LPC and RPC handles are created, see 
     <a href="https://msdn.microsoft.com/en-us/library/Aa370974(v=VS.85).aspx">LPC and RPC Handles</a> and 
     <a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>.

<b>ClusterControl</b> is one of the 
     <a href="https://msdn.microsoft.com/en-us/library/Aa369310(v=VS.85).aspx">control code functions</a>. For more information on 
     control codes and control code functions, see 
     <a href="https://msdn.microsoft.com/en-us/library/Aa372956(v=VS.85).aspx">Using Control Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa369093(v=VS.85).aspx">Cluster Control Codes</a>



<a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>
 

 

