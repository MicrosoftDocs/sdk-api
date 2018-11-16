---
UID: NF:clusapi.CloseClusterNotifyPort
title: CloseClusterNotifyPort function
author: windows-sdk-content
description: Closes a notification port established through CreateClusterNotifyPort.
old-location: mscs\closeclusternotifyport.htm
tech.root: MsCS
ms.assetid: abf7145c-780b-4ec7-babb-0e3975520f4a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CloseClusterNotifyPort, CloseClusterNotifyPort function [Failover Cluster], PCLUSAPI_CLOSE_CLUSTER_NOTIFY_PORT, PCLUSAPI_CLOSE_CLUSTER_NOTIFY_PORT function [Failover Cluster], _wolf_closeclusternotifyport, clusapi/CloseClusterNotifyPort, clusapi/PCLUSAPI_CLOSE_CLUSTER_NOTIFY_PORT, mscs.closeclusternotifyport
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
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
 - CloseClusterNotifyPort
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- CloseClusterNotifyPort
: 
---

# CloseClusterNotifyPort function


## -description


Closes a notification port established through  <a href="https://msdn.microsoft.com/90e85f5d-54b4-48a5-bb5b-e46eb14781bb">CreateClusterNotifyPort</a>. The <b>PCLUSAPI_CLOSE_CLUSTER_NOTIFY_PORT</b> type defines a pointer to this function.


## -parameters




### -param hChange [in]

Handle to the notification port to close.


## -returns



This function always returns <b>TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/90e85f5d-54b4-48a5-bb5b-e46eb14781bb">CreateClusterNotifyPort</a>



<a href="https://msdn.microsoft.com/9f650e2e-0651-4d1c-9314-b83f4f805f04">GetClusterNotify</a>



<a href="https://msdn.microsoft.com/ddf0e01c-08e9-4e32-b012-76c8a41037a7">RegisterClusterNotify</a>
 

 

