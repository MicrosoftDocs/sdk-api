---
UID: NS:resapi.RESOURCE_STATUS_EX
title: RESOURCE_STATUS_EX
author: windows-sdk-content
description: Contains information about a resource that is being brought online or taken offline. This structure is used as a parameter to the callback function SetResourceStatusEx.
old-location: mscs\resource_status_ex.htm
old-project: mscs
ms.assetid: CBEBF870-B413-400C-A485-FD093358FB67
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PRESOURCE_STATUS_EX, CLUSRESDLL_STATUS_INSUFFICIENT_MEMORY, CLUSRESDLL_STATUS_INSUFFICIENT_OTHER_RESOURCES, CLUSRESDLL_STATUS_INSUFFICIENT_PROCESSOR, CLUSRESDLL_STATUS_NETWORK_NOT_AVAILABLE, CLUSRESDLL_STATUS_OFFLINE_BUSY, CLUSRESDLL_STATUS_OFFLINE_DESTINATION_REJECTED, CLUSRESDLL_STATUS_OFFLINE_DESTINATION_THROTTLED, CLUSRESDLL_STATUS_OFFLINE_SOURCE_THROTTLED, PRESOURCE_STATUS_EX, PRESOURCE_STATUS_EX structure pointer [Failover Cluster], RESOURCE_STATUS_EX, RESOURCE_STATUS_EX structure [Failover Cluster], STATUS_INVALID_PARAMETERS, mscs.resource_status_ex, resapi/PRESOURCE_STATUS_EX, resapi/RESOURCE_STATUS_EX"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: resapi.h
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
tech.root: 
req.typenames: RESOURCE_STATUS_EX, *PRESOURCE_STATUS_EX
topic_type:
 - kbSyntax
api_type:
 - <TBD>
api_location:
 -
api_name:
 - RESOURCE_STATUS_EX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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
 

 

