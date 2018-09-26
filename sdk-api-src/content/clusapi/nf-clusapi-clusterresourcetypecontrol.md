---
UID: NF:clusapi.ClusterResourceTypeControl
title: ClusterResourceTypeControl function
author: windows-sdk-content
description: Initiates an operation affecting a resource type. The operation performed depends on the control code passed to the dwControlCode parameter.
old-location: mscs\clusterresourcetypecontrol.htm
tech.root: mscs
ms.assetid: 79f4949d-e5ef-4d2e-ac11-0e30b6c566fd
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: ClusterResourceTypeControl, ClusterResourceTypeControl function [Failover Cluster], _wolf_clusterresourcetypecontrol, clusapi/ClusterResourceTypeControl, mscs.clusterresourcetypecontrol
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
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - ClusterResourceTypeControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterResourceTypeControl function


## -description


Initiates an operation affecting a <a href="https://msdn.microsoft.com/en-us/library/Aa372279(v=VS.85).aspx">resource type</a>. The 
    operation performed depends on the <a href="https://msdn.microsoft.com/en-us/library/Aa369307(v=VS.85).aspx">control code</a> passed to the 
    <i>dwControlCode</i> parameter.


## -parameters




### -param hCluster [in]

Handle to the cluster containing the resource type identified in 
       <i>lpszResourceTypeName</i>.


### -param lpszResourceTypeName [in]

Pointer to a <b>NULL</b>-terminated Unicode string containing the name of the resource 
       type to be affected.


### -param hHostNode [in, optional]

Handle to the node hosting the affected resource type.


### -param dwControlCode [in]

A <a href="https://msdn.microsoft.com/en-us/library/Aa372309(v=VS.85).aspx">resource type control code</a> specifying 
       the operation to be performed. For the syntax associated with a control code, refer to  
       <a href="https://msdn.microsoft.com/en-us/library/Aa369308(v=VS.85).aspx">Control Code Architecture</a> and the following 
       topics:

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367498(v=VS.85).aspx">CLUSCTL_RESOURCE_TYPE_ENUM_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367499(v=VS.85).aspx">CLUSCTL_RESOURCE_TYPE_ENUM_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367503(v=VS.85).aspx">CLUSCTL_RESOURCE_TYPE_GET_CHARACTERISTICS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367504(v=VS.85).aspx">CLUSCTL_RESOURCE_TYPE_GET_CLASS_INFO</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367505(v=VS.85).aspx">CLUSCTL_RESOURCE_TYPE_GET_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367506(v=VS.85).aspx">CLUSCTL_RESOURCE_TYPE_GET_COMMON_PROPERTY_FMTS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367507(v=VS.85).aspx">CLUSCTL_RESOURCE_TYPE_GET_COMMON_RESOURCE_PROPERTY_FMTS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367508(v=VS.85).aspx">CLUSCTL_RESOURCE_TYPE_GET_CRYPTO_CHECKPOINTS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367509(v=VS.85).aspx">CLUSCTL_RESOURCE_TYPE_GET_FLAGS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367510(v=VS.85).aspx">CLUSCTL_RESOURCE_TYPE_GET_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367511(v=VS.85).aspx">CLUSCTL_RESOURCE_TYPE_GET_PRIVATE_PROPERTY_FMTS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367512(v=VS.85).aspx">CLUSCTL_RESOURCE_TYPE_GET_PRIVATE_RESOURCE_PROPERTY_FMTS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367645(v=VS.85).aspx">CLUSCTL_RESOURCE_TYPE_GET_REGISTRY_CHECKPOINTS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367647(v=VS.85).aspx">CLUSCTL_RESOURCE_TYPE_GET_REQUIRED_DEPENDENCIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367651(v=VS.85).aspx">CLUSCTL_RESOURCE_TYPE_GET_RO_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367653(v=VS.85).aspx">CLUSCTL_RESOURCE_TYPE_GET_RO_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367661(v=VS.85).aspx">CLUSCTL_RESOURCE_TYPE_QUERY_DELETE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367665(v=VS.85).aspx">CLUSCTL_RESOURCE_TYPE_SET_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367668(v=VS.85).aspx">CLUSCTL_RESOURCE_TYPE_SET_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367675(v=VS.85).aspx">CLUSCTL_RESOURCE_TYPE_STORAGE_GET_AVAILABLE_DISKS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Hh920945(v=VS.85).aspx">CLUSCTL_RESOURCE_TYPE_STORAGE_GET_RESOURCEID</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367677(v=VS.85).aspx">CLUSCTL_RESOURCE_TYPE_UNKNOWN</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367682(v=VS.85).aspx">CLUSCTL_RESOURCE_TYPE_VALIDATE_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367685(v=VS.85).aspx">CLUSCTL_RESOURCE_TYPE_VALIDATE_PRIVATE_PROPERTIES</a>
</li>
</ul>

### -param lpInBuffer [in, optional]

Pointer to the input buffer with information needed for the operation, or <b>NULL</b> if 
       no information is needed.


### -param nInBufferSize [in]

Number of bytes in the buffer pointed to by <i>lpInBuffer</i>.


### -param lpOutBuffer [out, optional]

Pointer to the output buffer with information resulting from the operation, or 
      <b>NULL</b> if nothing will be returned.


### -param nOutBufferSize [in]

Number of bytes in the output buffer pointed to by <i>lpOutBuffer</i>, or zero if the 
       caller does not know how much data will be returned.


### -param lpBytesReturned [out, optional]

Pointer to the number of bytes in the buffer pointed to by <i>lpOutBuffer</i> that were 
       actually filled in as a result of the operation. The caller can pass <b>NULL</b> for 
       <i>lpBytesReturned</i> if 
       <b>ClusterResourceTypeControl</b> does not need 
       to pass back the number of bytes in the output buffer.


## -returns



The function returns one of the following values.




## -remarks



When <b>ClusterResourceTypeControl</b> returns 
     <b>ERROR_MORE_DATA</b>, set <i>nOutBufferSize</i> to the number of bytes 
     pointed to by <i>lpBytesReturned</i>, and call the function again.

Do not pass LPC and RPC handles to the same function call. Otherwise, the call will raise an RPC exception and 
     can have additional destructive effects. For information on how LPC and RPC handles are created, see 
     <a href="https://msdn.microsoft.com/en-us/library/Aa370974(v=VS.85).aspx">LPC and RPC Handles</a> and 
     <a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>.

<b>ClusterResourceTypeControl</b> is one of the 
     <a href="https://msdn.microsoft.com/en-us/library/Aa369310(v=VS.85).aspx">control code functions</a>. For more information on 
     control codes and control code functions, see 
     <a href="https://msdn.microsoft.com/en-us/library/Aa372956(v=VS.85).aspx">Using Control Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa372309(v=VS.85).aspx">Resource Type Control Codes</a>
 

 

