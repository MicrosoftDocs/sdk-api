---
UID: NC:clusapi.PCLUSAPI_CLOSE_CLUSTER_NET_INTERFACE
title: PCLUSAPI_CLOSE_CLUSTER_NET_INTERFACE
author: windows-sdk-content
description: Closes a network interface handle.
old-location: mscs\closeclusternetinterface.htm
old-project: mscs
ms.assetid: e5978e81-790a-4ca7-92b7-d19af31f222e
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: PCLUSAPI_CLOSE_CLUSTER_NET_INTERFACE, PCLUSAPI_CLOSE_CLUSTER_NET_INTERFACE callback, PCLUSAPI_CLOSE_CLUSTER_NET_INTERFACE callback function [Failover Cluster], _wolf_closeclusternetinterface, clusapi/PCLUSAPI_CLOSE_CLUSTER_NET_INTERFACE, mscs.closeclusternetinterface
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: Sources
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ClusAPI.h
api_name:
 - PCLUSAPI_CLOSE_CLUSTER_NET_INTERFACE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_CLOSE_CLUSTER_NET_INTERFACE callback function


## -description


Closes a  <a href="https://msdn.microsoft.com/en-us/library/Aa371519(v=VS.85).aspx">network interface</a> handle. The <b>PCLUSAPI_CLOSE_CLUSTER_NET_INTERFACE</b> type defines a pointer to this function.


## -parameters




### -param hNetInterface [in]

Handle of the network interface to close.


## -returns





Returns BOOL that ...






## -see-also




<a href="https://msdn.microsoft.com/1198ad57-ea47-428f-8867-061afbfc7709">OpenClusterNetInterface</a>
 

 

