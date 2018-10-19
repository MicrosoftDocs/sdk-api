---
UID: NF:clusapi.ClusterResourceGetEnumCountEx
title: ClusterResourceGetEnumCountEx function
author: windows-sdk-content
description: Returns the number of cluster objects that are associated with a resource enumeration handle.
old-location: mscs\clusterresourcegetenumcountex.htm
tech.root: mscs
ms.assetid: 97C22642-F968-4E41-90BC-28DF8DF5886C
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: ClusterResourceGetEnumCountEx, ClusterResourceGetEnumCountEx function [Failover Cluster], PCLUSAPI_CLUSTER_RESOURCE_GET_ENUM_COUNT_EX, PCLUSAPI_CLUSTER_RESOURCE_GET_ENUM_COUNT_EX function [Failover Cluster], clusapi/ClusterResourceGetEnumCountEx, clusapi/PCLUSAPI_CLUSTER_RESOURCE_GET_ENUM_COUNT_EX, mscs.clusterresourcegetenumcountex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - ClusterResourceGetEnumCountEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterResourceGetEnumCountEx function


## -description


Returns the number of  <a href="https://msdn.microsoft.com/en-us/library/Aa369115(v=VS.85).aspx">cluster objects</a>  that are associated with a  <a href="https://msdn.microsoft.com/en-us/library/Aa372152(v=VS.85).aspx">resource</a> enumeration handle.


## -parameters




### -param hResourceEnumEx [in]

The handle to a resource enumeration. This handle is obtained from 
the <a href="https://msdn.microsoft.com/B43460F1-4BFE-48E0-889A-56370320E4E6">ClusterResourceOpenEnumEx</a> function. A valid handle is required. This parameter cannot be <b>NULL</b>.


## -returns



The number of objects that are associated with the enumeration handle.




## -see-also




<a href="https://msdn.microsoft.com/B43460F1-4BFE-48E0-889A-56370320E4E6">ClusterResourceOpenEnumEx</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa372262(v=VS.85).aspx">Failover Cluster Resource Management Functions</a>
 

 

