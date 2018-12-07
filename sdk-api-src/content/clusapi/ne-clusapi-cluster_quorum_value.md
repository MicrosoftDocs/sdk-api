---
UID: NE:clusapi.CLUSTER_QUORUM_VALUE
title: CLUSTER_QUORUM_VALUE
author: windows-sdk-content
description: Enumerates values returned by the ClusterControl function with the CLUSCTL_CLUSTER_CHECK_VOTER_DOWN or the CLUSCTL_CLUSTER_CHECK_VOTER_EVICT control codes.
old-location: mscs\cluster_quorum_value.htm
tech.root: mscs
ms.assetid: 5b5310f5-b4f4-4c1e-82ad-3bbf3ebc511b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CLUSTER_QUORUM_LOST, CLUSTER_QUORUM_MAINTAINED, CLUSTER_QUORUM_VALUE, CLUSTER_QUORUM_VALUE enumeration [Failover Cluster], msclus/CLUSTER_QUORUM_LOST, msclus/CLUSTER_QUORUM_MAINTAINED, msclus/CLUSTER_QUORUM_VALUE, mscs.cluster_quorum_value
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: clusapi.h
req.include-header: ClusAPI.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msclus.h
api_name:
 - CLUSTER_QUORUM_VALUE
product: Windows
targetos: Windows
req.typenames: CLUSTER_QUORUM_VALUE
req.redist: 
---

# CLUSTER_QUORUM_VALUE enumeration


## -description


Enumerates values returned by the 
    <a href="https://msdn.microsoft.com/en-us/library/Aa368833(v=VS.85).aspx">ClusterControl</a> function with the 
    <a href="https://msdn.microsoft.com/en-us/library/Bb309078(v=VS.85).aspx">CLUSCTL_CLUSTER_CHECK_VOTER_DOWN</a> or the 
    <a href="https://msdn.microsoft.com/en-us/library/Bb309079(v=VS.85).aspx">CLUSCTL_CLUSTER_CHECK_VOTER_EVICT</a> 
    control codes.


## -enum-fields




### -field CLUSTER_QUORUM_MAINTAINED

The quorum will be maintained.


### -field CLUSTER_QUORUM_LOST

The quorum will be lost.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb309078(v=VS.85).aspx">CLUSCTL_CLUSTER_CHECK_VOTER_DOWN</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb309079(v=VS.85).aspx">CLUSCTL_CLUSTER_CHECK_VOTER_EVICT</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa368833(v=VS.85).aspx">ClusterControl</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb309147(v=VS.85).aspx">Failover Cluster Enumerations</a>
 

 

