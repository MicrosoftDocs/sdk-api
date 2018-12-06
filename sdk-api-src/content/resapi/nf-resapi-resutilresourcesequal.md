---
UID: NF:resapi.ResUtilResourcesEqual
title: ResUtilResourcesEqual function
author: windows-sdk-content
description: Tests whether two resource handles represent the same resource. The PRESUTIL_RESOURCES_EQUAL type defines a pointer to this function.
old-location: mscs\resutilresourcesequal.htm
tech.root: mscs
ms.assetid: a34bbe15-f13f-4034-b2f1-fea3e58c579e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PRESUTIL_RESOURCES_EQUAL, PRESUTIL_RESOURCES_EQUAL function [Failover Cluster], ResUtilResourcesEqual, ResUtilResourcesEqual function [Failover Cluster], _wolf_resutilresourcesequal, mscs.resutilresourcesequal, resapi/PRESUTIL_RESOURCES_EQUAL, resapi/ResUtilResourcesEqual
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: resapi.h
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
req.lib: ResUtils.lib
req.dll: ResUtils.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ResUtils.dll
api_name:
 - ResUtilResourcesEqual
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ResUtilResourcesEqual function


## -description


Tests whether two resource handles represent the same  <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a>. The <b>PRESUTIL_RESOURCES_EQUAL</b> type defines a pointer to this function.


## -parameters




### -param hSelf [in]

Handle to one of the resources.


### -param hResource [in]

Handle to the other resource.


## -returns



If the resources are equal, the function returns <b>TRUE</b>.

If the resources are not equal, 
the function returns <b>FALSE</b>.




## -remarks



The  <b>ResUtilResourcesEqual</b> utility function compares the two resources by retrieving their names. To retrieve the names,  <b>ResUtilResourcesEqual</b> passes the  <a href="https://msdn.microsoft.com/d1d4b8cf-ab74-449c-aaf7-9bc7ef09b789">CLUSCTL_RESOURCE_GET_NAME</a> control code to the  <a href="https://msdn.microsoft.com/a98ca55a-6535-48cf-a925-5005baa01b94">ClusterResourceControl</a> function. If the names are the same, the resources are equal.

Do not pass LPC and RPC handles in the same function call. If you do, the call will raise an RPC exception and can result in additional destructive effects. For information on how LPC and RPC handles are created, see  <a href="https://msdn.microsoft.com/709effda-5ff1-439e-805a-9169ca63c182">Using Object Handles</a> and  <a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>.




## -see-also




<a href="https://msdn.microsoft.com/d1d4b8cf-ab74-449c-aaf7-9bc7ef09b789">CLUSCTL_RESOURCE_GET_NAME</a>



<a href="https://msdn.microsoft.com/a98ca55a-6535-48cf-a925-5005baa01b94">ClusterResourceControl</a>
 

 

