---
UID: NC:clusapi.PCLUSAPI_CLOSE_CLUSTER_NETWORK
title: PCLUSAPI_CLOSE_CLUSTER_NETWORK
author: windows-sdk-content
description: Closes a network handle.
old-location: mscs\closeclusternetwork.htm
old-project: mscs
ms.assetid: 2d112729-1306-45ff-8845-43032a55ca1c
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: PCLUSAPI_CLOSE_CLUSTER_NETWORK, PCLUSAPI_CLOSE_CLUSTER_NETWORK callback, PCLUSAPI_CLOSE_CLUSTER_NETWORK callback function [Failover Cluster], _wolf_closeclusternetwork, clusapi/PCLUSAPI_CLOSE_CLUSTER_NETWORK, mscs.closeclusternetwork
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
 - PCLUSAPI_CLOSE_CLUSTER_NETWORK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_CLOSE_CLUSTER_NETWORK callback function


## -description


Closes a  <a href="https://msdn.microsoft.com/en-us/library/Aa371501(v=VS.85).aspx">network</a> handle. The <b>PCLUSAPI_CLOSE_CLUSTER_NETWORK</b> type defines a pointer to this function.


## -parameters




### -param hNetwork [in]

Handle to the network to close.


## -returns





Returns BOOL that ...






## -see-also




<a href="https://msdn.microsoft.com/a888ca91-e56f-42bc-81c5-9235c6fd5172">OpenClusterNetwork</a>
 

 

