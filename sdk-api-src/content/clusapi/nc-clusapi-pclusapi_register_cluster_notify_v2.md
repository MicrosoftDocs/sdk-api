---
UID: NC:clusapi.PCLUSAPI_REGISTER_CLUSTER_NOTIFY_V2
title: PCLUSAPI_REGISTER_CLUSTER_NOTIFY_V2
author: windows-sdk-content
description: Registers an event type with a notification port by adding the notification key to the event type.
old-location: mscs\registerclusternotifyv2.htm
old-project: mscs
ms.assetid: DCBE285A-7386-4922-8599-19149FEBBD9F
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PCLUSAPI_REGISTER_CLUSTER_NOTIFY_V2, PCLUSAPI_REGISTER_CLUSTER_NOTIFY_V2 function [Failover Cluster], RegisterClusterNotifyV2, RegisterClusterNotifyV2 function [Failover Cluster], clusapi/PCLUSAPI_REGISTER_CLUSTER_NOTIFY_V2, clusapi/RegisterClusterNotifyV2, mscs.registerclusternotifyv2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: clusapi.h
req.include-header: 
req.redist: 
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
req.typenames: Sources
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

# PCLUSAPI_REGISTER_CLUSTER_NOTIFY_V2 callback function


## -description


Registers an 
    event type with a notification port by adding the notification key to the  event type.


## -parameters




### -param hChange [in]

A handle to a notification port that is created with the 
      <a href="https://msdn.microsoft.com/81FE17A9-DE1C-4CDD-BE7D-50EA202D5AAC">CreateClusterNotifyPortV2</a> function.


### -param Filter [in]

A <a href="https://msdn.microsoft.com/en-us/library/Dn622942(v=VS.85).aspx">NOTIFY_FILTER_AND_TYPE</a> structure that specifies the event type to create.


### -param hObject [in]

A handle to the <a href="https://msdn.microsoft.com/en-us/library/Aa369115(v=VS.85).aspx">failover cluster object</a> 
       that is affected by the event as specified in the <i>dwFilterType</i> parameter. The type of handle 
      depends on the value of <i>dwFilterType</i>.


### -param dwNotifyKey [in]

The notification key that is returned from the  
      <a href="https://msdn.microsoft.com/9f650e2e-0651-4d1c-9314-b83f4f805f04">GetClusterNotify</a>  function when the requested event 
      occurs.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
       <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error code</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa369107(v=VS.85).aspx">Failover Cluster Management Function</a>
 

 

