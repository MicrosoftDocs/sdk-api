---
UID: NF:clusapi.ClusterNetworkControl
title: ClusterNetworkControl function
author: windows-sdk-content
description: Initiates an operation on a network. The operation performed depends on the control code passed to the dwControlCode parameter.
old-location: mscs\clusternetworkcontrol.htm
tech.root: mscs
ms.assetid: df0d7b45-4d8b-4780-944a-0fbba670f99a
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ClusterNetworkControl, ClusterNetworkControl function [Failover Cluster], _wolf_clusternetworkcontrol, clusapi/ClusterNetworkControl, mscs.clusternetworkcontrol
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
 - ClusterNetworkControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterNetworkControl function


## -description


Initiates 
    an operation on a <a href="https://msdn.microsoft.com/en-us/library/Aa371501(v=VS.85).aspx">network</a>. The operation performed depends on the 
    <a href="https://msdn.microsoft.com/en-us/library/Aa369307(v=VS.85).aspx">control code</a> passed to the 
    <i>dwControlCode</i> parameter.


## -parameters




### -param hNetwork [in]

Handle to the network to be affected by the operation.


### -param hHostNode [in, optional]

If non-<b>NULL</b>, handle to the <a href="https://msdn.microsoft.com/en-us/library/Aa371745(v=VS.85).aspx">node</a> 
       hosting the affected network. If <b>NULL</b>, the local node performs the operation. 
       Specifying <i>hHostNode</i> is optional.


### -param dwControlCode [in]

A <a href="https://msdn.microsoft.com/en-us/library/Aa371518(v=VS.85).aspx">network control code</a> specifying the 
       operation to be performed. For the syntax associated with a control code, refer to  
       <a href="https://msdn.microsoft.com/en-us/library/Aa369308(v=VS.85).aspx">Control Code Architecture</a> and the following 
       topics:


<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367397(v=VS.85).aspx">CLUSCTL_NETWORK_ENUM_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367398(v=VS.85).aspx">CLUSCTL_NETWORK_ENUM_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367399(v=VS.85).aspx">CLUSCTL_NETWORK_GET_CHARACTERISTICS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367400(v=VS.85).aspx">CLUSCTL_NETWORK_GET_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367401(v=VS.85).aspx">CLUSCTL_NETWORK_GET_COMMON_PROPERTY_FMTS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367402(v=VS.85).aspx">CLUSCTL_NETWORK_GET_FLAGS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367403(v=VS.85).aspx">CLUSCTL_NETWORK_GET_ID</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367404(v=VS.85).aspx">CLUSCTL_NETWORK_GET_NAME</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367405(v=VS.85).aspx">CLUSCTL_NETWORK_GET_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367406(v=VS.85).aspx">CLUSCTL_NETWORK_GET_PRIVATE_PROPERTY_FMTS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367407(v=VS.85).aspx">CLUSCTL_NETWORK_GET_RO_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367408(v=VS.85).aspx">CLUSCTL_NETWORK_GET_RO_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367409(v=VS.85).aspx">CLUSCTL_NETWORK_SET_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367410(v=VS.85).aspx">CLUSCTL_NETWORK_SET_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367411(v=VS.85).aspx">CLUSCTL_NETWORK_UNKNOWN</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367412(v=VS.85).aspx">CLUSCTL_NETWORK_VALIDATE_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367413(v=VS.85).aspx">CLUSCTL_NETWORK_VALIDATE_PRIVATE_PROPERTIES</a>
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


### -param lpBytesReturned [in, out, optional]

Returns the actual size (in bytes) of the data resulting from the operation. If this information is not 
       needed, pass <b>NULL</b> for <i>lpBytesReturned</i>.


## -returns



The function returns one of the following values.




## -remarks



If <b>ClusterNetworkControl</b> returns 
     <b>ERROR_MORE_DATA</b>, set <i>nOutBufferSize</i> to the number of bytes 
     pointed to by <i>lpBytesReturned</i>, and call the function again.

Do not pass LPC and RPC handles to the same function call. Otherwise, the call will raise an RPC exception and 
     can have additional destructive effects. For information on how LPC and RPC handles are created, see 
     <a href="https://msdn.microsoft.com/en-us/library/Aa370974(v=VS.85).aspx">LPC and RPC Handles</a> and 
     <a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>.

<b>ClusterNetworkControl</b> is one of the 
     <a href="https://msdn.microsoft.com/en-us/library/Aa369310(v=VS.85).aspx">control code functions</a>. For more information on 
     control codes and control code functions, see 
     <a href="https://msdn.microsoft.com/en-us/library/Aa372956(v=VS.85).aspx">Using Control Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa371518(v=VS.85).aspx">Network Control Codes</a>



<a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>
 

 

