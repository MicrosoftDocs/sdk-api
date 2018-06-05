---
UID: NC:clusapi.PCLUSAPI_CLOSE_CLUSTER_RESOURCE
title: PCLUSAPI_CLOSE_CLUSTER_RESOURCE
author: windows-sdk-content
description: Closes a resource handle.
old-location: mscs\closeclusterresource.htm
old-project: MsCS
ms.assetid: dbefd7f9-3499-45b3-a5c8-d0000632f61c
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: PCLUSAPI_CLOSE_CLUSTER_RESOURCE, PCLUSAPI_CLOSE_CLUSTER_RESOURCE callback, PCLUSAPI_CLOSE_CLUSTER_RESOURCE callback function [Failover Cluster], _wolf_closeclusterresource, clusapi/PCLUSAPI_CLOSE_CLUSTER_RESOURCE, mscs.closeclusterresource
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
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ClusAPI.h
api_name:
-	PCLUSAPI_CLOSE_CLUSTER_RESOURCE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_CLOSE_CLUSTER_RESOURCE callback function


## -description


Closes a  <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> handle. The <b>PCLUSAPI_CLOSE_CLUSTER_RESOURCE</b> type defines a pointer to this function.


## -parameters




### -param hResource [in]

Handle to the resource to be closed.


## -returns





Returns BOOL that ...






## -see-also




<a href="https://msdn.microsoft.com/c9fe8fa8-57d7-4866-8113-694dc44dae22">CreateClusterResource</a>



<a href="https://msdn.microsoft.com/c699cb00-b999-45b8-b9db-570150e1a65e">OpenClusterResource</a>
 

 

