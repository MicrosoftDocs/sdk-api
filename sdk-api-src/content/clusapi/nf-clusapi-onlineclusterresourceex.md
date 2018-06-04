---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

