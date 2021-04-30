---
UID: NS:resapi.RESOURCE_STATUS_EX
title: RESOURCE_STATUS_EX (resapi.h)
description: Contains information about a resource that is being brought online or taken offline. This structure is used as a parameter to the callback function SetResourceStatusEx.
helpviewer_keywords: ["*PRESOURCE_STATUS_EX","CLUSRESDLL_STATUS_INSUFFICIENT_MEMORY","CLUSRESDLL_STATUS_INSUFFICIENT_OTHER_RESOURCES","CLUSRESDLL_STATUS_INSUFFICIENT_PROCESSOR","CLUSRESDLL_STATUS_NETWORK_NOT_AVAILABLE","CLUSRESDLL_STATUS_OFFLINE_BUSY","CLUSRESDLL_STATUS_OFFLINE_DESTINATION_REJECTED","CLUSRESDLL_STATUS_OFFLINE_DESTINATION_THROTTLED","CLUSRESDLL_STATUS_OFFLINE_SOURCE_THROTTLED","PRESOURCE_STATUS_EX","PRESOURCE_STATUS_EX structure pointer [Failover Cluster]","RESOURCE_STATUS_EX","RESOURCE_STATUS_EX structure [Failover Cluster]","STATUS_INVALID_PARAMETERS","mscs.resource_status_ex","resapi/PRESOURCE_STATUS_EX","resapi/RESOURCE_STATUS_EX"]
old-location: mscs\resource_status_ex.htm
tech.root: MsCS
ms.assetid: CBEBF870-B413-400C-A485-FD093358FB67
ms.date: 12/05/2018
ms.keywords: '*PRESOURCE_STATUS_EX, CLUSRESDLL_STATUS_INSUFFICIENT_MEMORY, CLUSRESDLL_STATUS_INSUFFICIENT_OTHER_RESOURCES, CLUSRESDLL_STATUS_INSUFFICIENT_PROCESSOR, CLUSRESDLL_STATUS_NETWORK_NOT_AVAILABLE, CLUSRESDLL_STATUS_OFFLINE_BUSY, CLUSRESDLL_STATUS_OFFLINE_DESTINATION_REJECTED, CLUSRESDLL_STATUS_OFFLINE_DESTINATION_THROTTLED, CLUSRESDLL_STATUS_OFFLINE_SOURCE_THROTTLED, PRESOURCE_STATUS_EX, PRESOURCE_STATUS_EX structure pointer [Failover Cluster], RESOURCE_STATUS_EX, RESOURCE_STATUS_EX structure [Failover Cluster], STATUS_INVALID_PARAMETERS, mscs.resource_status_ex, resapi/PRESOURCE_STATUS_EX, resapi/RESOURCE_STATUS_EX'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RESOURCE_STATUS_EX, *PRESOURCE_STATUS_EX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RESOURCE_STATUS_EX
 - resapi/RESOURCE_STATUS_EX
 - PRESOURCE_STATUS_EX
 - resapi/PRESOURCE_STATUS_EX
dev_langs:
 - c++
topic_type:
 - kbSyntax
api_type:
 - <TBD>
api_location:
api_name:
 - RESOURCE_STATUS_EX
---

# RESOURCE_STATUS_EX structure


## -description

Contains information 
    about a <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> that is being brought online or taken offline. 
    This structure is used as a parameter to the callback function 
    <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pset_resource_status_routine_ex">SetResourceStatusEx</a>.

## -struct-fields

### -field ResourceState

A <a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_resource_state">CLUSTER_RESOURCE_STATE</a> enumeration value that describes the state of the resource.

### -field CheckPoint

A value set by the <a href="/previous-versions/windows/desktop/mscs/resource-dlls">resource DLL</a> to flag a status 
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

The <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pset_resource_status_routine_ex">SetResourceStatusEx</a> function received invalid parameters.



#### CLUSRESDLL_STATUS_NETWORK_NOT_AVAILABLE (0x00000100)

The network is not available.

<b>Windows Server 2012:  </b>This value is not supported before Windows Server 2012 R2.

### -field WaitHint

This member is not being used at this time.

<b>Windows Server 2012:  </b>This member was added in Windows Server 2012 R2.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/resource-dll-structures">Resource DLL Structures</a>