---
UID: NC:clusapi.PCLUSAPI_CLOSE_CLUSTER_NOTIFY_PORT
title: PCLUSAPI_CLOSE_CLUSTER_NOTIFY_PORT
author: windows-driver-content
description: Closes a notification port established through CreateClusterNotifyPort.
old-location: mscs\closeclusternotifyport.htm
old-project: MsCS
ms.assetid: abf7145c-780b-4ec7-babb-0e3975520f4a
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: PCLUSAPI_CLOSE_CLUSTER_NOTIFY_PORT, PCLUSAPI_CLOSE_CLUSTER_NOTIFY_PORT callback, PCLUSAPI_CLOSE_CLUSTER_NOTIFY_PORT callback function [Failover Cluster], _wolf_closeclusternotifyport, clusapi/PCLUSAPI_CLOSE_CLUSTER_NOTIFY_PORT, mscs.closeclusternotifyport
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
req.typenames: Sources
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ClusAPI.h
api_name:
-	PCLUSAPI_CLOSE_CLUSTER_NOTIFY_PORT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_CLOSE_CLUSTER_NOTIFY_PORT callback function


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
 

 

