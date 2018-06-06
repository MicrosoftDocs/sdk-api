---
UID: NF:clusapi.ClusterControl
title: ClusterControl function
author: windows-sdk-content
description: Initiates an operation that affects a cluster.
old-location: mscs\clustercontrol.htm
old-project: MsCS
ms.assetid: 7ef06c95-8d9d-4b87-a6d8-d6a2d49523ee
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: ClusterControl, ClusterControl function [Failover Cluster], _wolf_clustercontrol, clusapi/ClusterControl, mscs.clustercontrol
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
tech.root: 
req.typenames: SR_REPLICATED_DISK_TYPE, *PSR_REPLICATED_DISK_TYPE
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
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
---

# ClusterControl function


## -description


Initiates an 
    operation that affects a <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a>. The operation 
    performed depends on the <a href="https://msdn.microsoft.com/47618915-0985-4415-b7d4-5959fb27eb9f">control code</a> passed to the 
    <i>dwControlCode</i> parameter.


## -parameters




### -param hCluster [in]

Handle to the cluster to be affected.


### -param hHostNode [in, optional]

If non-<b>NULL</b>, handle to the node to perform the operation represented by the control 
       code. If <b>NULL</b>, the local node performs the operation. Specifying 
       <i>hHostNode</i> is optional.


### -param dwControlCode [in]

A <a href="https://msdn.microsoft.com/cabd9d59-7ace-4081-9de1-7645c882a64d">cluster control code</a> from the 
       <a href="https://msdn.microsoft.com/b5ce8c3c-3a5d-4785-a3ce-b8b37c6c5dc8">CLUSCTL_CLUSTER_CODES</a> enumeration that specifies 
       the operation to be performed. For the syntax associated with a control code, refer to 
       <a href="https://msdn.microsoft.com/d107f743-8ce8-4c0c-b7a2-24a70ffbc0f3">Control Code Architecture</a> and the following 
       topics:


<ul>
<li>
<a href="https://msdn.microsoft.com/4987c8c1-7f5a-4b4a-8fba-55457922b641">CLUSCTL_CLUSTER_CHECK_VOTER_DOWN</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e87d5598-01f5-4d33-aa8c-e9c059cb9716">CLUSCTL_CLUSTER_CHECK_VOTER_EVICT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/B00D4725-AD1B-415D-A774-1216F0017FFF">CLUSCTL_CLUSTER_CLEAR_NODE_CONNECTION_INFO</a>
</li>
<li>
<a href="https://msdn.microsoft.com/03fadf36-9a76-496e-a48b-c083c958b870">CLUSCTL_CLUSTER_ENUM_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1009b6b5-47b0-475d-97a2-cd68243d3072">CLUSCTL_CLUSTER_ENUM_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8b4d68b5-01f5-438a-93d7-853f19bad1d4">CLUSCTL_CLUSTER_GET_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ba8a9445-b955-481a-9c6c-7457fa38a746">CLUSCTL_CLUSTER_GET_FQDN</a>
</li>
<li>
<a href="https://msdn.microsoft.com/29f87a9c-98e2-46c0-94a0-634924e07930">CLUSCTL_CLUSTER_GET_COMMON_PROPERTY_FMTS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/852025e6-9fa1-47a5-8e7b-272cd453ce19">CLUSCTL_CLUSTER_GET_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c92d8fc4-44e4-4026-9e67-58c4ad5cfaf0">CLUSCTL_CLUSTER_GET_PRIVATE_PROPERTY_FMTS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/045d39bc-085f-4d09-9854-d694df4d0a6a">CLUSCTL_CLUSTER_GET_RO_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a51019bc-f412-4c91-8e6d-b32200c2e39c">CLUSCTL_CLUSTER_GET_RO_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0e470934-f1c1-40b2-93b7-10a9b3de3032">CLUSCTL_CLUSTER_GET_SHARED_VOLUME_ID</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c58d6390-3f22-4ad4-a568-d79a787eefdf">CLUSCTL_CLUSTER_SET_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e7e471b8-1df4-4b46-bdac-d0acadd86910">CLUSCTL_CLUSTER_SET_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ebf8820a-109e-47fe-94ed-4fb1377597d5">CLUSCTL_CLUSTER_SHUTDOWN</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1b5467c0-1cf2-4678-8e1a-000ab053d334">CLUSCTL_CLUSTER_UNKNOWN</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a4db891b-bf8c-42bd-b366-cddd89c279ba">CLUSCTL_CLUSTER_VALIDATE_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/afbe9278-5484-4081-b345-1885268bd38a">CLUSCTL_CLUSTER_VALIDATE_PRIVATE_PROPERTIES</a>
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
     <a href="https://msdn.microsoft.com/0fdb2024-9b04-4a38-baf9-3cdabba9bf8c">LPC and RPC Handles</a> and 
     <a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>.

<b>ClusterControl</b> is one of the 
     <a href="https://msdn.microsoft.com/89ae667e-6ad9-453e-b370-b3d6a67172a2">control code functions</a>. For more information on 
     control codes and control code functions, see 
     <a href="https://msdn.microsoft.com/20f87f60-6237-459a-93bc-f599391e65b0">Using Control Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/cabd9d59-7ace-4081-9de1-7645c882a64d">Cluster Control Codes</a>



<a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>
 

 

