---
UID: NF:clusapi.ClusterResourceTypeControlAsUser
title: ClusterResourceTypeControlAsUser function
author: windows-sdk-content
description: Initiates an operation affecting a resource type.
old-location: mscs\clusterresourcetypecontrolasuser.htm
tech.root: MsCS
ms.assetid: 9F39952F-4B91-4C06-A789-D92F1F8462A4
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ClusterResourceTypeControlAsUser, ClusterResourceTypeControlAsUser function [Failover Cluster], clusapi/ClusterResourceTypeControlAsUser, mscs.clusterresourcetypecontrolasuser
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
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
 - ClusterResourceTypeControlAsUser
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterResourceTypeControlAsUser function


## -description


Initiates an operation affecting a 
    <a href="https://msdn.microsoft.com/d02e4f51-7b86-451a-a51c-ea850ae464d1">resource type</a>.

The 
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

A <a href="https://msdn.microsoft.com/71ec60fd-67ec-4932-983b-f78c6b552954">resource control code</a>, enumerated by the 
       <a href="https://msdn.microsoft.com/c34eda93-9389-4bf0-9e8f-7a80f10a1081">CLUSCTL_RESOURCE_TYPE_CODES</a> enumeration, 
       specifying the operation to be performed. For the syntax associated with a control code, refer to  the link on 
       the <b>CLUSCTL_RESOURCE_TYPE_CODES</b> topic.


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
       <a href="https://msdn.microsoft.com/79f4949d-e5ef-4d2e-ac11-0e30b6c566fd">ClusterResourceTypeControl</a> does not need 
       to pass back the number of bytes in the output buffer.


## -returns



The function returns one of the following values.




## -remarks



When <a href="https://msdn.microsoft.com/79f4949d-e5ef-4d2e-ac11-0e30b6c566fd">ClusterResourceTypeControl</a> returns 
     <b>ERROR_MORE_DATA</b>, set <i>nOutBufferSize</i> to the number of bytes 
     pointed to by <i>lpBytesReturned</i>, and call the function again.

Do not pass LPC and RPC handles to the same function call. Otherwise, the call will raise an RPC exception and 
     can have additional destructive effects. For information on how LPC and RPC handles are created, see 
     <a href="https://msdn.microsoft.com/0fdb2024-9b04-4a38-baf9-3cdabba9bf8c">LPC and RPC Handles</a> and 
     <a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>.


<a href="https://msdn.microsoft.com/79f4949d-e5ef-4d2e-ac11-0e30b6c566fd">ClusterResourceTypeControl</a> is one of the 
     <a href="https://msdn.microsoft.com/89ae667e-6ad9-453e-b370-b3d6a67172a2">control code functions</a>. For more information on 
     control codes and control code functions, see 
     <a href="https://msdn.microsoft.com/20f87f60-6237-459a-93bc-f599391e65b0">Using Control Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>



<a href="https://msdn.microsoft.com/a854829d-ed05-40a0-b7c8-c3e5ab888220">Resource Type Control Codes</a>
 

 

