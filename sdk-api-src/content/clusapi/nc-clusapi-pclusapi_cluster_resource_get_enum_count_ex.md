---
UID: NC:clusapi.PCLUSAPI_CLUSTER_RESOURCE_GET_ENUM_COUNT_EX
title: PCLUSAPI_CLUSTER_RESOURCE_GET_ENUM_COUNT_EX
author: windows-driver-content
description: Returns the number of cluster objects that are associated with a resource enumeration handle.
old-location: mscs\clusterresourcegetenumcountex.htm
old-project: MsCS
ms.assetid: 97C22642-F968-4E41-90BC-28DF8DF5886C
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: PCLUSAPI_CLUSTER_RESOURCE_GET_ENUM_COUNT_EX, PCLUSAPI_CLUSTER_RESOURCE_GET_ENUM_COUNT_EX callback, PCLUSAPI_CLUSTER_RESOURCE_GET_ENUM_COUNT_EX callback function [Failover Cluster], clusapi/PCLUSAPI_CLUSTER_RESOURCE_GET_ENUM_COUNT_EX, mscs.clusterresourcegetenumcountex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
req.typenames: Sources
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ClusAPI.h
api_name:
-	PCLUSAPI_CLUSTER_RESOURCE_GET_ENUM_COUNT_EX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_CLUSTER_RESOURCE_GET_ENUM_COUNT_EX callback function


## -description


Returns the number of  <a href="https://msdn.microsoft.com/609cc002-2db9-4ec6-a802-8f7bdbb11b90">cluster objects</a>  that are associated with a  <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> enumeration handle.


## -parameters




### -param hResourceEnumEx [in]

The handle to a resource enumeration. This handle is obtained from 
the <a href="https://msdn.microsoft.com/B43460F1-4BFE-48E0-889A-56370320E4E6">ClusterResourceOpenEnumEx</a> function. A valid handle is required. This parameter cannot be <b>NULL</b>.


## -returns



The number of objects that are associated with the enumeration handle.




## -see-also




<a href="https://msdn.microsoft.com/B43460F1-4BFE-48E0-889A-56370320E4E6">ClusterResourceOpenEnumEx</a>



<a href="https://msdn.microsoft.com/d1f7360d-f592-49fb-b3b4-60d93afd7c6f">Failover Cluster Resource Management Functions</a>
 

 

