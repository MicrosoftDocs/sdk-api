---
UID: NC:clusapi.PCLUSAPI_CLUSTER_RESOURCE_CLOSE_ENUM_EX
title: PCLUSAPI_CLUSTER_RESOURCE_CLOSE_ENUM_EX
author: windows-driver-content
description: Closes a handle to a resource enumeration.
old-location: mscs\clusterresourcecloseenumex.htm
old-project: MsCS
ms.assetid: 643CA960-F4F1-4028-B0A3-5258E9421D62
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: PCLUSAPI_CLUSTER_RESOURCE_CLOSE_ENUM_EX, PCLUSAPI_CLUSTER_RESOURCE_CLOSE_ENUM_EX callback function [Failover Cluster], clusapi/PCLUSAPI_CLUSTER_RESOURCE_CLOSE_ENUM_EX, mscs.clusterresourcecloseenumex
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
req.typenames: LOG_MANAGEMENT_CALLBACKS, *PLOG_MANAGEMENT_CALLBACKS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ClusAPI.h
api_name:
-	PCLUSAPI_CLUSTER_RESOURCE_CLOSE_ENUM_EX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_CLUSTER_RESOURCE_CLOSE_ENUM_EX callback


## -description


Closes a handle to a  resource enumeration.


## -parameters




### -param hResourceEnumEx [in]

The handle to a resource enumeration  to  close.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.
     If the operation fails, 
the function returns a different <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -see-also




<a href="https://msdn.microsoft.com/d1f7360d-f592-49fb-b3b4-60d93afd7c6f">Failover Cluster Resource Management Functions</a>
 

 

