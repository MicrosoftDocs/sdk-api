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

# POFFLINE_V2_ROUTINE callback function


## -description


Marks a <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> as unavailable for use after cleanup 
    processing is complete. The <b>POFFLINE_V2_ROUTINE</b> type defines a pointer to 
    this function.


## -parameters




### -param Resource [in]

A resource identifier for the resource to be taken offline.


### -param DestinationNodeName [in, optional]

The name of the node that is to contain the resource when the operation completes.


### -param OfflineFlags [in]

A bitmask of flags that specify settings for this operation. This parameter can be set to one or more  of the following values:



#### CLUS_RESDLL_OFFLINE_IGNORE_RESOURCE_STATUS (0x00000001)

Perform the operation even if the resource indicates that it should be locked.



#### CLUS_RESDLL_OFFLINE_RETURN_TO_SOURCE_NODE_ON_ERROR (0x00000002)

If the resource experiences an error, return it to the source node.



#### CLUS_RESDLL_OFFLINE_QUEUE_ENABLED (0x00000004)

Queue the operation if it is delayed by a resource DLL, and then retry the operation until it completes or is cancelled by the client.



#### CLUS_RESDLL_OFFLINE_RETURNING_TO_SOURCE_NODE_BECAUSE_OF_ERROR (0x00000008)

Indicate that the resource experienced an error, and is returning  to the source node.



#### CLUS_RESDLL_OFFLINE_DUE_TO_EMBEDDED_FAILURE (0x00000010)

Indicate that there was an embedded failure.



#### CLUS_RESDLL_OFFLINE_IGNORE_NETWORK_CONNECTIVITY (0x00000020)

Perform the operation even if there is network error.

<b>Windows Server 2012:  </b>This value is not supported before Windows Server 2012 R2.



#### CLUS_RESDLL_OFFLINE_DO_NOT_UPDATE_PERSISTENT_STATE (0x00000040)

Do not update the persistent state of the resource.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This value is not supported before Windows Server 2016.


### -param InBuffer [in, optional]

A pointer to a buffer that contains  data for the operation; otherwise <b>NULL</b> if the operation does not require data.


### -param InBufferSize [in]

The size of the <i>InBuffer</i> parameter, in bytes.


### -param Reserved [in]

Reserved.


## -returns



If the operation was not successful for other reasons, 
       this function returns one of the 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/933d7b97-b5be-4c84-a983-41d1fd935c19">Resource DLL Entry Point Functions</a>
 

 

