---
UID: NF:clusapi.ClusterNodeControl
title: ClusterNodeControl function
author: windows-sdk-content
description: Initiates an operation that affects a node. The operation performed depends on the control code passed to the dwControlCode parameter.
old-location: mscs\clusternodecontrol.htm
tech.root: mscs
ms.assetid: f6fc8525-a2d3-4643-9372-548df5e30900
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ClusterNodeControl, ClusterNodeControl function [Failover Cluster], _wolf_clusternodecontrol, clusapi/ClusterNodeControl, mscs.clusternodecontrol
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
 - ClusterNodeControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterNodeControl function


## -description


Initiates an 
    operation that affects a <a href="https://msdn.microsoft.com/en-us/library/Aa371745(v=VS.85).aspx">node</a>. The operation performed depends on the 
    <a href="https://msdn.microsoft.com/en-us/library/Aa369307(v=VS.85).aspx">control code</a> passed to the 
    <i>dwControlCode</i> parameter.


## -parameters




### -param hNode [in]

Handle to the node to be affected.


### -param hHostNode [in, optional]

If non-<b>NULL</b>, handle to the node that will perform the operation instead of the node 
       specified in <i>hNode</i>. If <b>NULL</b>, the node that handles the call 
       performs the operation.


### -param dwControlCode [in]

A <a href="https://msdn.microsoft.com/en-us/library/Aa371759(v=VS.85).aspx">node control code</a> specifying the operation to be 
       performed. For the syntax associated with a control code, refer to  
       <a href="https://msdn.microsoft.com/en-us/library/Aa369308(v=VS.85).aspx">Control Code Architecture</a> and the following 
       topics:

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367414(v=VS.85).aspx">CLUSCTL_NODE_ENUM_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367415(v=VS.85).aspx">CLUSCTL_NODE_ENUM_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367416(v=VS.85).aspx">CLUSCTL_NODE_GET_CHARACTERISTICS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367418(v=VS.85).aspx">CLUSCTL_NODE_GET_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367419(v=VS.85).aspx">CLUSCTL_NODE_GET_COMMON_PROPERTY_FMTS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/f86835e1-2721-46ab-bd85-599e91d1d5bd">CLUSCTL_NODE_GET_FLAGS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0222665c-f029-40d9-b568-b27ad6e78dfc">CLUSCTL_NODE_GET_ID</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9ad0c5ec-294a-4236-b179-77cafbaa95f2">CLUSCTL_NODE_GET_NAME</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b22f281d-d88d-41bb-ab49-e7168e6e9f95">CLUSCTL_NODE_GET_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/f66f3966-8364-42be-b59e-b6b9a034c362">CLUSCTL_NODE_GET_PRIVATE_PROPERTY_FMTS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e7466dff-e20e-442e-a91c-b07c34d172d8">CLUSCTL_NODE_GET_RO_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/170509ac-6373-40a4-8370-835bf5d647df">CLUSCTL_NODE_GET_RO_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367429(v=VS.85).aspx">CLUSCTL_NODE_SET_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367433(v=VS.85).aspx">CLUSCTL_NODE_SET_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367435(v=VS.85).aspx">CLUSCTL_NODE_UNKNOWN</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367436(v=VS.85).aspx">CLUSCTL_NODE_VALIDATE_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367440(v=VS.85).aspx">CLUSCTL_NODE_VALIDATE_PRIVATE_PROPERTIES</a>
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
       needed, pass <b>NULL</b> for <i>lpBytesReturned</i>.


## -returns



The function returns one of the following values.




## -remarks



If <b>ClusterNodeControl</b> returns 
     <b>ERROR_MORE_DATA</b>, set <i>nOutBufferSize</i> to the number of bytes 
     pointed to by <i>lpBytesReturned</i> and call the function again.

Do not pass LPC and RPC handles to the same function call. Otherwise, the call will raise an RPC exception and 
     can have additional destructive effects. For information on how LPC and RPC handles are created, see 
     <a href="https://msdn.microsoft.com/en-us/library/Aa370974(v=VS.85).aspx">LPC and RPC Handles</a> and 
     <a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>.

<b>ClusterNodeControl</b> is one of the 
     <a href="https://msdn.microsoft.com/en-us/library/Aa369310(v=VS.85).aspx">control code functions</a>. For more information on 
     control codes and control code functions, see 
     <a href="https://msdn.microsoft.com/en-us/library/Aa372956(v=VS.85).aspx">Using Control Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa371759(v=VS.85).aspx">Node Control Codes</a>



<a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>
 

 

