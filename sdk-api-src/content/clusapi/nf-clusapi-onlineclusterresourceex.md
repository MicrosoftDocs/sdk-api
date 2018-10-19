---
UID: NF:clusapi.OnlineClusterResourceEx
title: OnlineClusterResourceEx function
author: windows-sdk-content
description: Brings an offline or failed resource online.
old-location: mscs\onlineclusterresourceex.htm
tech.root: mscs
ms.assetid: 8A41D266-0FBD-4063-9C79-E22924129989
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: CLUSAPI_GROUP_ONLINE_IGNORE_RESOURCE_STATUS, CLUSAPI_RESOURCE_ONLINE_BEST_POSSIBLE_NODE, CLUSAPI_RESOURCE_ONLINE_DO_NOT_UPDATE_PERSISTENT_STATE, CLUSAPI_RESOURCE_ONLINE_NECESSARY_FOR_QUORUM, OnlineClusterResourceEx, OnlineClusterResourceEx function [Failover Cluster], clusapi/OnlineClusterResourceEx, mscs.onlineclusterresourceex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-0.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - OnlineClusterResourceEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# OnlineClusterResourceEx function


## -description


Brings an offline or failed  <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> online.


## -parameters




### -param hResource [in]

The handle to the resource to bring online.


### -param dwOnlineFlags [in]

A flag that specifies settings for the resource that is to be brought online.



#### CLUSAPI_GROUP_ONLINE_IGNORE_RESOURCE_STATUS (0x00000001)

The server is to ignore locked mode for the resource.



#### CLUSAPI_RESOURCE_ONLINE_DO_NOT_UPDATE_PERSISTENT_STATE (0x00000002)

Do not update the persistent state of the resource.



#### CLUSAPI_RESOURCE_ONLINE_NECESSARY_FOR_QUORUM (0x00000004)

The resource must be brought online to maintain a quorum.



#### CLUSAPI_RESOURCE_ONLINE_BEST_POSSIBLE_NODE (0x00000008)

The cluster service is to determine the node that will host the resource when it is brought online.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This value is not supported before Windows Server 2016.



#### 0

The server is  not to  ignore locked mode for the resource.


### -param lpInBuffer [in, optional]

A pointer to the input buffer that receives instructions for the operation. The <i>lpInBuffer</i>  parameter is formatted as a property list.


### -param cbInBufferSize [in]

The size of <i>lpInBuffer</i>, in bytes.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following is a possible error code.




## -see-also




<a href="https://msdn.microsoft.com/d1f7360d-f592-49fb-b3b4-60d93afd7c6f">Failover Cluster Resource Management Functions</a>
 

 

