---
UID: NE:clusapi.CLUSTER_GROUP_AUTOFAILBACK_TYPE
title: CLUSTER_GROUP_AUTOFAILBACK_TYPE
author: windows-sdk-content
description: Used by the AutoFailbackType group common property to specify whether the group should be failed back to the node identified as its preferred owner when that node comes back online following a failover.
old-location: mscs\cluster_group_autofailback_type.htm
tech.root: MsCS
ms.assetid: d7ba9298-25fc-454b-8583-196f84622cc5
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CGAFT, CGAFT enumeration [Failover Cluster], CLUSTER_GROUP_AUTOFAILBACK_TYPE, CLUSTER_GROUP_AUTOFAILBACK_TYPE enumeration [Failover Cluster], ClusterGroupAllowFailback, ClusterGroupFailbackTypeCount, ClusterGroupPreventFailback, _CLUSTER_GROUP_AUTOFAILBACK_TYPE, _CLUSTER_GROUP_AUTOFAILBACK_TYPE enumeration [Failover Cluster], clusapi/CGAFT, clusapi/CLUSTER_GROUP_AUTOFAILBACK_TYPE, clusapi/ClusterGroupAllowFailback, clusapi/ClusterGroupFailbackTypeCount, clusapi/ClusterGroupPreventFailback, clusapi/_CLUSTER_GROUP_AUTOFAILBACK_TYPE, msclus/CGAFT, msclus/CLUSTER_GROUP_AUTOFAILBACK_TYPE, msclus/ClusterGroupAllowFailback, msclus/ClusterGroupFailbackTypeCount, msclus/ClusterGroupPreventFailback, msclus/_CLUSTER_GROUP_AUTOFAILBACK_TYPE, mscs.cluster_group_autofailback_type
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
 - MsClus.h
api_name:
 - CLUSTER_GROUP_AUTOFAILBACK_TYPE
product: Windows
targetos: Windows
req.typenames: CLUSTER_GROUP_AUTOFAILBACK_TYPE, CGAFT
req.redist: 
---

# CLUSTER_GROUP_AUTOFAILBACK_TYPE enumeration


## -description


Used by the 
    <a href="https://msdn.microsoft.com/en-us/library/Aa369653(v=VS.85).aspx">AutoFailbackType</a> group 
    <a href="https://msdn.microsoft.com/en-us/library/Aa369191(v=VS.85).aspx">common property</a> to specify whether the group should be 
    failed back to the <a href="https://msdn.microsoft.com/en-us/library/Aa371745(v=VS.85).aspx">node</a> identified as its preferred owner when that 
    node comes back online following a <a href="https://msdn.microsoft.com/en-us/library/Aa369573(v=VS.85).aspx">failover</a>.


## -enum-fields




### -field ClusterGroupPreventFailback

Prevents <a href="https://msdn.microsoft.com/en-us/library/Aa369571(v=VS.85).aspx">failback</a>.


### -field ClusterGroupAllowFailback

Allows failback (requires a preferred owners list for the group).


### -field ClusterGroupFailbackTypeCount

Defines a maximum group property value. It is not supported by the 
       <a href="https://msdn.microsoft.com/en-us/library/Aa369653(v=VS.85).aspx">AutoFailbackType</a> group property.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa369653(v=VS.85).aspx">AutoFailbackType</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb309147(v=VS.85).aspx">Failover Cluster Enumerations</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa369191(v=VS.85).aspx">common property</a>
 

 

