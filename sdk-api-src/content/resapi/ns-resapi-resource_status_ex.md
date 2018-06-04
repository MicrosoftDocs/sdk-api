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

# RESOURCE_STATUS_EX structure


## -description


Contains information 
    about a <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> that is being brought online or taken offline. 
    This structure is used as a parameter to the callback function 
    <a href="https://msdn.microsoft.com/3733F912-9D43-489B-91D8-7128D0F5D1A4">SetResourceStatusEx</a>.


## -struct-fields




### -field ResourceState

A <a href="https://msdn.microsoft.com/bd5dee18-a06f-4e46-a27e-c907b1c25a68">CLUSTER_RESOURCE_STATE</a> enumeration value that describes the state of the resource.


### -field CheckPoint

A value set by the <a href="https://msdn.microsoft.com/e1434102-afaf-4a35-887e-a434c628bd90">resource DLL</a> to flag a status 
      report as new.


### -field EventHandle

A handle to an event that indicates when the resource has failed.


### -field ApplicationSpecificErrorCode

TBD


### -field Flags

A bitmask of flags that specify settings for the operation. This member can contain one or more of the following values:



#### CLUSRESDLL_STATUS_OFFLINE_BUSY (0x00000001)

The resource is busy.



#### CLUSRESDLL_STATUS_OFFLINE_SOURCE_THROTTLED (0x00000002)

The source is  being throttled.



#### CLUSRESDLL_STATUS_OFFLINE_DESTINATION_THROTTLED (0x00000004)

The destination is being throttled.



#### CLUSRESDLL_STATUS_OFFLINE_DESTINATION_REJECTED (0x00000008)

The destination was rejected.



#### CLUSRESDLL_STATUS_INSUFFICIENT_MEMORY (0x00000010)

There was insufficient memory to perform the operation.



#### CLUSRESDLL_STATUS_INSUFFICIENT_PROCESSOR (0x00000020)

There was insufficient processing resources to perform the operation.



#### CLUSRESDLL_STATUS_INSUFFICIENT_OTHER_RESOURCES (0x00000040)

There was insufficient resources (other than processing or memory resources) to perform the operation.



#### STATUS_INVALID_PARAMETERS (0x00000080)

The <a href="https://msdn.microsoft.com/3733F912-9D43-489B-91D8-7128D0F5D1A4">SetResourceStatusEx</a> function received invalid parameters.



#### CLUSRESDLL_STATUS_NETWORK_NOT_AVAILABLE (0x00000100)

The network is not available.

<b>Windows Server 2012:  </b>This value is not supported before Windows Server 2012 R2.


### -field WaitHint

This member is not being used at this time.

<b>Windows Server 2012:  </b>This member was added in Windows Server 2012 R2.


## -see-also




<a href="https://msdn.microsoft.com/9ab4b974-28b5-4f33-a7c4-b9b2472059aa">Resource DLL Structures</a>
 

 

