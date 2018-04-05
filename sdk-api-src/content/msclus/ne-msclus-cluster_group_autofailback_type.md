---
UID: NE:msclus.CLUSTER_GROUP_AUTOFAILBACK_TYPE
title: CLUSTER_GROUP_AUTOFAILBACK_TYPE
author: windows-driver-content
description: Used by the AutoFailbackType group common property to specify whether the group should be failed back to the node identified as its preferred owner when that node comes back online following a failover.
old-location: mscs\cluster_group_autofailback_type.htm
old-project: MsCS
ms.assetid: d7ba9298-25fc-454b-8583-196f84622cc5
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: CGAFT, CGAFT enumeration [Failover Cluster], CLUSTER_GROUP_AUTOFAILBACK_TYPE, CLUSTER_GROUP_AUTOFAILBACK_TYPE enumeration [Failover Cluster], ClusterGroupAllowFailback, ClusterGroupFailbackTypeCount, ClusterGroupPreventFailback, _CLUSTER_GROUP_AUTOFAILBACK_TYPE, _CLUSTER_GROUP_AUTOFAILBACK_TYPE enumeration [Failover Cluster], clusapi/CGAFT, clusapi/CLUSTER_GROUP_AUTOFAILBACK_TYPE, clusapi/ClusterGroupAllowFailback, clusapi/ClusterGroupFailbackTypeCount, clusapi/ClusterGroupPreventFailback, clusapi/_CLUSTER_GROUP_AUTOFAILBACK_TYPE, msclus/CGAFT, msclus/CLUSTER_GROUP_AUTOFAILBACK_TYPE, msclus/ClusterGroupAllowFailback, msclus/ClusterGroupFailbackTypeCount, msclus/ClusterGroupPreventFailback, msclus/_CLUSTER_GROUP_AUTOFAILBACK_TYPE, mscs.cluster_group_autofailback_type
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: msclus.h
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
req.typenames: CLUSTER_GROUP_AUTOFAILBACK_TYPE, CGAFT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ClusAPI.h
-	MsClus.h
api_name:
-	CLUSTER_GROUP_AUTOFAILBACK_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# CLUSTER_GROUP_AUTOFAILBACK_TYPE enumeration


## -description


Used by the 
    <a href="https://msdn.microsoft.com/cd06c375-2684-4943-8587-692e655b44a2">AutoFailbackType</a> group 
    <a href="https://msdn.microsoft.com/5341d390-69dd-4e84-a443-f35a4b6c0bab">common property</a> to specify whether the group should be 
    failed back to the <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> identified as its preferred owner when that 
    node comes back online following a <a href="https://msdn.microsoft.com/6722d075-02e0-4817-abc3-dce8951c17da">failover</a>.


## -enum-fields




### -field ClusterGroupPreventFailback

Prevents <a href="https://msdn.microsoft.com/dcb53180-86bf-4cba-bf93-9c19cbc127b8">failback</a>.


### -field ClusterGroupAllowFailback

Allows failback (requires a preferred owners list for the group).


### -field ClusterGroupFailbackTypeCount

Defines a maximum group property value. It is not supported by the 
       <a href="https://msdn.microsoft.com/cd06c375-2684-4943-8587-692e655b44a2">AutoFailbackType</a> group property.


## -see-also




<a href="https://msdn.microsoft.com/cd06c375-2684-4943-8587-692e655b44a2">AutoFailbackType</a>



<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>



<a href="https://msdn.microsoft.com/5341d390-69dd-4e84-a443-f35a4b6c0bab">common property</a>
 

 

