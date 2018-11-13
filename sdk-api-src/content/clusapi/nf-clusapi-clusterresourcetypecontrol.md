---
UID: NF:clusapi.ClusterResourceTypeControl
title: ClusterResourceTypeControl function
author: windows-sdk-content
description: Initiates an operation affecting a resource type. The operation performed depends on the control code passed to the dwControlCode parameter.
old-location: mscs\clusterresourcetypecontrol.htm
tech.root: mscs
ms.assetid: 79f4949d-e5ef-4d2e-ac11-0e30b6c566fd
ms.author: windowssdkdev
ms.date: 11/06/2018
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


Initiates an operation affecting a <a href="https://msdn.microsoft.com/d02e4f51-7b86-451a-a51c-ea850ae464d1">resource type</a>. The 
    operation performed depends on the <a href="https://msdn.microsoft.com/47618915-0985-4415-b7d4-5959fb27eb9f">control code</a> passed to the 
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

A <a href="https://msdn.microsoft.com/a854829d-ed05-40a0-b7c8-c3e5ab888220">resource type control code</a> specifying 
       the operation to be performed. For the syntax associated with a control code, refer to  
       <a href="https://msdn.microsoft.com/d107f743-8ce8-4c0c-b7a2-24a70ffbc0f3">Control Code Architecture</a> and the following 
       topics:

<ul>
<li>
<a href="https://msdn.microsoft.com/ca04e4c9-0fc8-48f5-a604-9d726f2bc102">CLUSCTL_RESOURCE_TYPE_ENUM_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/44b4752f-69aa-4082-9912-02ffa7a18d0c">CLUSCTL_RESOURCE_TYPE_ENUM_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d968810f-cd95-43a8-8897-43ebf0bd6f08">CLUSCTL_RESOURCE_TYPE_GET_CHARACTERISTICS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/db811070-9de6-4368-b9b5-ac17259d68a1">CLUSCTL_RESOURCE_TYPE_GET_CLASS_INFO</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6d628d94-5ab9-4300-9490-cfe9924ad62e">CLUSCTL_RESOURCE_TYPE_GET_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8978a813-7bd0-4759-9aa2-f97fe63e1577">CLUSCTL_RESOURCE_TYPE_GET_COMMON_PROPERTY_FMTS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/cc4975c4-dec4-44d2-9cd3-f00dcd8720ed">CLUSCTL_RESOURCE_TYPE_GET_COMMON_RESOURCE_PROPERTY_FMTS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2db7f65c-e5ad-4b59-bf52-2d4212d34e97">CLUSCTL_RESOURCE_TYPE_GET_CRYPTO_CHECKPOINTS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a7ed60d5-cafe-4436-8cd3-e95eb89677a8">CLUSCTL_RESOURCE_TYPE_GET_FLAGS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/28c5043e-259e-4bcb-aad1-92b8cc6b8845">CLUSCTL_RESOURCE_TYPE_GET_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ddc3d89d-83ca-4d6f-92f5-0ad3917fdd1b">CLUSCTL_RESOURCE_TYPE_GET_PRIVATE_PROPERTY_FMTS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/cc3dc11a-1019-4449-87da-45b1b254fec4">CLUSCTL_RESOURCE_TYPE_GET_PRIVATE_RESOURCE_PROPERTY_FMTS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/239c8d1b-014d-45c3-9aef-37c4f76f07dc">CLUSCTL_RESOURCE_TYPE_GET_REGISTRY_CHECKPOINTS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/01a1b0bc-e831-4535-b782-2a24bd6adf22">CLUSCTL_RESOURCE_TYPE_GET_REQUIRED_DEPENDENCIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/25db960a-c37f-429a-81e4-02ce64599f3c">CLUSCTL_RESOURCE_TYPE_GET_RO_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/483115b5-f1f9-4650-b54b-f32e45992196">CLUSCTL_RESOURCE_TYPE_GET_RO_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/aee8a682-4049-4b5a-80e3-2f51392439e5">CLUSCTL_RESOURCE_TYPE_QUERY_DELETE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/001903bf-9bcf-483e-b280-41c745f52365">CLUSCTL_RESOURCE_TYPE_SET_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/24f76cb4-be47-4ac5-b96f-3fd9a63cf264">CLUSCTL_RESOURCE_TYPE_SET_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2df1eeb4-ecad-4065-866c-545476a43d9b">CLUSCTL_RESOURCE_TYPE_STORAGE_GET_AVAILABLE_DISKS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/47EE15C6-E92D-4FEE-B2A2-5C94875B7D96">CLUSCTL_RESOURCE_TYPE_STORAGE_GET_RESOURCEID</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ec23ea78-8cd5-4366-a65d-98eb46c90362">CLUSCTL_RESOURCE_TYPE_UNKNOWN</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a9e117fa-82c6-42d1-a09e-270d307e2548">CLUSCTL_RESOURCE_TYPE_VALIDATE_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4d509cad-9fc8-40c4-a557-2ebb65855f78">CLUSCTL_RESOURCE_TYPE_VALIDATE_PRIVATE_PROPERTIES</a>
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
     <a href="https://msdn.microsoft.com/0fdb2024-9b04-4a38-baf9-3cdabba9bf8c">LPC and RPC Handles</a> and 
     <a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>.

<b>ClusterResourceTypeControl</b> is one of the 
     <a href="https://msdn.microsoft.com/89ae667e-6ad9-453e-b370-b3d6a67172a2">control code functions</a>. For more information on 
     control codes and control code functions, see 
     <a href="https://msdn.microsoft.com/20f87f60-6237-459a-93bc-f599391e65b0">Using Control Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>



<a href="https://msdn.microsoft.com/a854829d-ed05-40a0-b7c8-c3e5ab888220">Resource Type Control Codes</a>
 

 

