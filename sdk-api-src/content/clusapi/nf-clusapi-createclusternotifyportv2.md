---
UID: NF:clusapi.CreateClusterNotifyPortV2
title: CreateClusterNotifyPortV2 function
author: windows-sdk-content
description: Creates or modifies a notification port. For information about notification ports, see Receiving Cluster Events.
old-location: mscs\createclusternotifyportv2.htm
tech.root: mscs
ms.assetid: 81FE17A9-DE1C-4CDD-BE7D-50EA202D5AAC
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: CreateClusterNotifyPortV2, CreateClusterNotifyPortV2 function [Failover Cluster], PCLUSAPI_CREATE_CLUSTER_NOTIFY_PORT_V2, PCLUSAPI_CREATE_CLUSTER_NOTIFY_PORT_V2 function [Failover Cluster], clusapi/CreateClusterNotifyPortV2, clusapi/PCLUSAPI_CREATE_CLUSTER_NOTIFY_PORT_V2, mscs.createclusternotifyportv2
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
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - CreateClusterNotifyPortV2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateClusterNotifyPortV2 function


## -description


Creates 
    or modifies a notification port. For information about  notification ports, see 
    <a href="https://msdn.microsoft.com/6d69cdd8-b29a-40c5-94c6-908b9bea22ef">Receiving Cluster Events</a>.


## -parameters




### -param hChange [in]

A handle to a notification port or <b>INVALID_HANDLE_VALUE</b>, indicating that a new handle 
       should be created. If the <i>hChange</i>  parameter is an existing handle, the events that are specified in 
       the <i>dwFilter</i> parameter are added to the notification port.


### -param hCluster [in]

A handle to the <a href="c_gly.htm">cluster</a> to be associated with the 
       notification port that is  identified by the  <i>hChange</i>    parameter or 
       <b>INVALID_HANDLE_VALUE</b>, indicating that the notification port should not be associated 
       with a cluster. If the  <i>hChange</i>  parameter  is not set to 
       <b>INVALID_HANDLE_VALUE</b>, the <i>hCluster</i>  parameter cannot be set to 
       <b>INVALID_HANDLE_VALUE</b>.


### -param Filters [in]

A pointer to the <a href="https://msdn.microsoft.com/E173F5D8-955B-44FF-980E-CEF536A87AF5">NOTIFY_FILTER_AND_TYPE</a> structure that specifies the  type of notifications that the port can accept.


### -param dwFilterCount [in]

The number of filters that are  specified by the <i>Filters</i> parameter.


### -param dwNotifyKey [in]

A user-specified value to associate with the retrieval of notifications from the notification port. The 
       <i>dwNotifyKey</i>  parameter is returned from 
       <a href="https://msdn.microsoft.com/0AF127E1-D517-4F4B-B797-40822B3B236F">GetClusterNotifyV2</a> when an event of one of the types 
       that are    specified in <i>Filters</i> occurs.


## -returns



If the operation succeeds, the function returns a notification port handle.

If the operation fails, the 
       function returns <b>NULL</b>. For more information about the error, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/1b3a3b23-39db-47b7-b4a8-17fc1ee45df6">Failover Cluster Management Function</a>
 

 

