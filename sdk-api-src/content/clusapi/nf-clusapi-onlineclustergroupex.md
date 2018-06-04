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

# OnlineClusterGroupEx function


## -description


Brings a  <a href="https://msdn.microsoft.com/library/windows/hardware/dn934674">group</a> online.


## -parameters




### -param hGroup [in]

A handle to the group to be brought online.


### -param hDestinationNode [in, optional]

A handle to the  <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> that is to host the group.


### -param dwOnlineFlags [in]

A flag that specifies settings for the resource that is to be brought online.



#### CLUSAPI_GROUP_ONLINE_IGNORE_RESOURCE_STATUS (0x00000001)

The server is to ignore locked mode for the resource.



#### CLUSAPI_GROUP_ONLINE_SYNCHRONOUS (0x00000002)

Use a synchronous operation to bring the group online.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This value was added in Windows Server 2016.



#### CLUSAPI_GROUP_ONLINE_BEST_POSSIBLE_NODE (0x00000004)

Let the cluster service is to determine the node that will host the group when it is brought online.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This value was added in Windows Server 2016.



#### 0

The server is  not to  ignore locked mode for the resource.


### -param lpInBuffer [in, optional]

A pointer to the input buffer that receives instructions for the operation.  The <i>lpInBuffer</i>  parameter is formatted as a property list.


### -param cbInBufferSize [in]

The size of the <i>lpInBuffer</i> parameter, in bytes.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following are possible error codes.




## -see-also




<a href="https://msdn.microsoft.com/a2336594-ac24-476e-94e8-460a31c1f643">Group Management Functions</a>
 

 

