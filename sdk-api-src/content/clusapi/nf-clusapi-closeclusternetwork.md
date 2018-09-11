---
UID: NF:clusapi.CloseClusterNetwork
title: CloseClusterNetwork function
author: windows-sdk-content
description: Closes a network handle.
old-location: mscs\closeclusternetwork.htm
tech.root: mscs
ms.assetid: 2d112729-1306-45ff-8845-43032a55ca1c
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CloseClusterNetwork, CloseClusterNetwork function [Failover Cluster], PCLUSAPI_CLOSE_CLUSTER_NETWORK, PCLUSAPI_CLOSE_CLUSTER_NETWORK function [Failover Cluster], _wolf_closeclusternetwork, clusapi/CloseClusterNetwork, clusapi/PCLUSAPI_CLOSE_CLUSTER_NETWORK, mscs.closeclusternetwork
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
api_name:
 - CloseClusterNetwork
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CloseClusterNetwork function


## -description


Closes a  <a href="https://msdn.microsoft.com/en-us/library/Aa371501(v=VS.85).aspx">network</a> handle. The <b>PCLUSAPI_CLOSE_CLUSTER_NETWORK</b> type defines a pointer to this function.


## -parameters




### -param hNetwork [in]

Handle to the network to close.


## -returns



This function returns BOOL.




## -see-also




<a href="https://msdn.microsoft.com/a888ca91-e56f-42bc-81c5-9235c6fd5172">OpenClusterNetwork</a>
 

 

