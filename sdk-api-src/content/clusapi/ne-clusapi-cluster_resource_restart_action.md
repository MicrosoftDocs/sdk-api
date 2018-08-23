---
UID: NE:clusapi.CLUSTER_RESOURCE_RESTART_ACTION
title: CLUSTER_RESOURCE_RESTART_ACTION
author: windows-sdk-content
description: Used by the RestartAction&#32;resource common property to specify the action to be taken by the cluster service if the resource fails.
old-location: mscs\cluster_resource_restart_action.htm
old-project: mscs
ms.assetid: 6300bdb7-2349-44f8-913a-dd84813bd3bd
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CLUSTER_RESOURCE_RESTART_ACTION, CLUSTER_RESOURCE_RESTART_ACTION enumeration [Failover Cluster], CRRA, CRRA enumeration [Failover Cluster], ClusterResourceDontRestart, ClusterResourceRestartActionCount, ClusterResourceRestartNoNotify, ClusterResourceRestartNotify, _CLUSTER_RESOURCE_RESTART_ACTION, _CLUSTER_RESOURCE_RESTART_ACTION enumeration [Failover Cluster], clusapi/CLUSTER_RESOURCE_RESTART_ACTION, clusapi/CRRA, clusapi/ClusterResourceDontRestart, clusapi/ClusterResourceRestartActionCount, clusapi/ClusterResourceRestartNoNotify, clusapi/ClusterResourceRestartNotify, clusapi/_CLUSTER_RESOURCE_RESTART_ACTION, msclus/CLUSTER_RESOURCE_RESTART_ACTION, msclus/CRRA, msclus/ClusterResourceDontRestart, msclus/ClusterResourceRestartActionCount, msclus/ClusterResourceRestartNoNotify, msclus/ClusterResourceRestartNotify, msclus/_CLUSTER_RESOURCE_RESTART_ACTION, mscs.cluster_resource_restart_action
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: clusapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: CluAdmEx.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CLUSTER_RESOURCE_RESTART_ACTION, CRRA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
 - MsClus.h
api_name:
 - CLUSTER_RESOURCE_RESTART_ACTION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# CLUSTER_RESOURCE_RESTART_ACTION enumeration


## -description


Used by the <a href="https://msdn.microsoft.com/en-us/library/Aa372202(v=VS.85).aspx">RestartAction</a> <a href="https://msdn.microsoft.com/en-us/library/Aa372230(v=VS.85).aspx">resource common property</a> to specify the action 
    to be taken by the <a href="https://msdn.microsoft.com/en-us/library/Aa369163(v=VS.85).aspx">cluster service</a> if the 
    <a href="https://msdn.microsoft.com/en-us/library/Aa372255(v=VS.85).aspx">resource fails</a>.


## -enum-fields




### -field ClusterResourceDontRestart

Do not restart the resource after a failure.


### -field ClusterResourceRestartNoNotify

Restart the resource after a failure. If the resource exceeds its restart threshold within its restart 
       period, do not attempt to <a href="https://msdn.microsoft.com/en-us/library/Aa369573(v=VS.85).aspx">failover</a> the 
       <a href="https://msdn.microsoft.com/en-us/library/Aa369645(v=VS.85).aspx">group</a> to another 
       <a href="https://msdn.microsoft.com/en-us/library/Aa371745(v=VS.85).aspx">node</a> in the 
       <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster</a>.


### -field ClusterResourceRestartNotify

Restart the resource after a failure. If the resource exceeds its restart threshold within its restart 
       period, attempt to fail over the group to another node in the cluster. This is the default setting.


### -field ClusterResourceRestartActionCount

Defines the maximum value of the 
       <a href="https://msdn.microsoft.com/en-us/library/Bb309167(v=VS.85).aspx">CLUSTER_RESOURCE_RESTART_ACTION</a> enumeration.  It is not a valid value for the 
       <a href="https://msdn.microsoft.com/en-us/library/Aa372202(v=VS.85).aspx">RestartAction</a> property.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb309147(v=VS.85).aspx">Failover Cluster Enumerations</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa372202(v=VS.85).aspx">RestartAction</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa372230(v=VS.85).aspx">resource common property</a>
 

 

