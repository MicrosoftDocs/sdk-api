---
UID: NF:clusapi.RegisterClusterNotifyV2
title: RegisterClusterNotifyV2 function
author: windows-sdk-content
description: Registers an event type with a notification port by adding the notification key to the event type.
old-location: mscs\registerclusternotifyv2.htm
old-project: mscs
ms.assetid: DCBE285A-7386-4922-8599-19149FEBBD9F
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: PCLUSAPI_REGISTER_CLUSTER_NOTIFY_V2, PCLUSAPI_REGISTER_CLUSTER_NOTIFY_V2 function [Failover Cluster], RegisterClusterNotifyV2, RegisterClusterNotifyV2 function [Failover Cluster], clusapi/PCLUSAPI_REGISTER_CLUSTER_NOTIFY_V2, clusapi/RegisterClusterNotifyV2, mscs.registerclusternotifyv2
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SR_REPLICATED_DISK_TYPE, *PSR_REPLICATED_DISK_TYPE
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
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
---

# RegisterClusterNotifyV2 function


## -description


Registers an 
    event type with a notification port by adding the notification key to the  event type.


## -parameters




### -param hChange [in]

A handle to a notification port that is created with the 
      <a href="https://msdn.microsoft.com/81FE17A9-DE1C-4CDD-BE7D-50EA202D5AAC">CreateClusterNotifyPortV2</a> function.


### -param Filter [in]

A <a href="https://msdn.microsoft.com/E173F5D8-955B-44FF-980E-CEF536A87AF5">NOTIFY_FILTER_AND_TYPE</a> structure that specifies the event type to create.


### -param hObject [in]

A handle to the <a href="https://msdn.microsoft.com/609cc002-2db9-4ec6-a802-8f7bdbb11b90">failover cluster object</a> 
       that is affected by the event as specified in the <i>dwFilterType</i> parameter. The type of handle 
      depends on the value of <i>dwFilterType</i>.


### -param dwNotifyKey [in]

The notification key that is returned from the  
      <a href="https://msdn.microsoft.com/9f650e2e-0651-4d1c-9314-b83f4f805f04">GetClusterNotify</a>  function when the requested event 
      occurs.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -see-also




<a href="https://msdn.microsoft.com/1b3a3b23-39db-47b7-b4a8-17fc1ee45df6">Failover Cluster Management Function</a>
 

 

