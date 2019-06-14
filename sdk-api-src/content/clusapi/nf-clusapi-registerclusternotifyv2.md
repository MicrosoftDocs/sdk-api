---
UID: NF:clusapi.RegisterClusterNotifyV2
title: RegisterClusterNotifyV2 function (clusapi.h)
author: windows-sdk-content
description: Registers an event type with a notification port by adding the notification key to the event type.
old-location: mscs\registerclusternotifyv2.htm
tech.root: MsCS
ms.assetid: DCBE285A-7386-4922-8599-19149FEBBD9F
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PCLUSAPI_REGISTER_CLUSTER_NOTIFY_V2, PCLUSAPI_REGISTER_CLUSTER_NOTIFY_V2 function [Failover Cluster], RegisterClusterNotifyV2, RegisterClusterNotifyV2 function [Failover Cluster], clusapi/PCLUSAPI_REGISTER_CLUSTER_NOTIFY_V2, clusapi/RegisterClusterNotifyV2, mscs.registerclusternotifyv2
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
 - RegisterClusterNotifyV2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RegisterClusterNotifyV2 function


## -description


Registers an 
    event type with a notification port by adding the notification key to the  event type.


## -parameters




### -param hChange [in]

A handle to a notification port that is created with the 
      <a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-createclusternotifyportv2">CreateClusterNotifyPortV2</a> function.


### -param Filter [in]

A <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/clusapi/ns-clusapi-_notify_filter_and_type">NOTIFY_FILTER_AND_TYPE</a> structure that specifies the event type to create.


### -param hObject [in]

A handle to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluster-objects">failover cluster object</a> 
       that is affected by the event as specified in the <i>dwFilterType</i> parameter. The type of handle 
      depends on the value of <i>dwFilterType</i>.


### -param dwNotifyKey [in]

The notification key that is returned from the  
      <a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-getclusternotify">GetClusterNotify</a>  function when the requested event 
      occurs.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
       <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error code</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluster-management-functions">Failover Cluster Management Function</a>
 

 

