---
UID: NC:clusapi.PCLUSAPI_CLOSE_CLUSTER_NET_INTERFACE
title: PCLUSAPI_CLOSE_CLUSTER_NET_INTERFACE
author: windows-driver-content
description: Closes a network interface handle.
old-location: mscs\closeclusternetinterface.htm
old-project: MsCS
ms.assetid: e5978e81-790a-4ca7-92b7-d19af31f222e
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: PCLUSAPI_CLOSE_CLUSTER_NET_INTERFACE, PCLUSAPI_CLOSE_CLUSTER_NET_INTERFACE callback, PCLUSAPI_CLOSE_CLUSTER_NET_INTERFACE callback function [Failover Cluster], _wolf_closeclusternetinterface, clusapi/PCLUSAPI_CLOSE_CLUSTER_NET_INTERFACE, mscs.closeclusternetinterface
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
-	PCLUSAPI_CLOSE_CLUSTER_NET_INTERFACE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_CLOSE_CLUSTER_NET_INTERFACE callback function


## -description


Closes a  <a href="https://msdn.microsoft.com/cc0cbbc3-e342-483e-9c94-4ee43f4d588d">network interface</a> handle. The <b>PCLUSAPI_CLOSE_CLUSTER_NET_INTERFACE</b> type defines a pointer to this function.


## -parameters




### -param hNetInterface [in]

Handle of the network interface to close.


## -returns





Returns BOOL that ...






## -see-also




<a href="https://msdn.microsoft.com/1198ad57-ea47-428f-8867-061afbfc7709">OpenClusterNetInterface</a>
 

 

