---
UID: NE:msclus.CLUSTER_RESOURCE_RESTART_ACTION
title: CLUSTER_RESOURCE_RESTART_ACTION
author: windows-sdk-content
description: Used by the RestartAction&#32;resource common property to specify the action to be taken by the cluster service if the resource fails.
old-location: mscs\cluster_resource_restart_action.htm
tech.root: mscs
ms.assetid: 6300bdb7-2349-44f8-913a-dd84813bd3bd
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: CLUSTER_RESOURCE_RESTART_ACTION, CLUSTER_RESOURCE_RESTART_ACTION enumeration [Failover Cluster], CRRA, CRRA enumeration [Failover Cluster], ClusterResourceDontRestart, ClusterResourceRestartActionCount, ClusterResourceRestartNoNotify, ClusterResourceRestartNotify, _CLUSTER_RESOURCE_RESTART_ACTION, _CLUSTER_RESOURCE_RESTART_ACTION enumeration [Failover Cluster], clusapi/CLUSTER_RESOURCE_RESTART_ACTION, clusapi/CRRA, clusapi/ClusterResourceDontRestart, clusapi/ClusterResourceRestartActionCount, clusapi/ClusterResourceRestartNoNotify, clusapi/ClusterResourceRestartNotify, clusapi/_CLUSTER_RESOURCE_RESTART_ACTION, msclus/CLUSTER_RESOURCE_RESTART_ACTION, msclus/CRRA, msclus/ClusterResourceDontRestart, msclus/ClusterResourceRestartActionCount, msclus/ClusterResourceRestartNoNotify, msclus/ClusterResourceRestartNotify, msclus/_CLUSTER_RESOURCE_RESTART_ACTION, mscs.cluster_resource_restart_action
ms.prod: windows
ms.technology: windows-sdk
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
 - CLUSTER_RESOURCE_RESTART_ACTION
product: Windows
targetos: Windows
req.typenames: CLUSTER_RESOURCE_RESTART_ACTION, CRRA
req.redist: 
---

# CLUSTER_RESOURCE_RESTART_ACTION enumeration


## -description


Used by the <a href="https://msdn.microsoft.com/88be809b-a338-490a-82f3-886bfc2e3f37">RestartAction</a> <a href="https://msdn.microsoft.com/b84fe8fe-a49e-4c3c-acbd-f9cfe5ac0782">resource common property</a> to specify the action 
    to be taken by the <a href="https://msdn.microsoft.com/90717d6e-f2a4-49a0-86b6-17de1c4bcfe4">cluster service</a> if the 
    <a href="https://msdn.microsoft.com/f18644d1-63ec-4920-b703-a3f149684508">resource fails</a>.


## -enum-fields




### -field ClusterResourceDontRestart

Do not restart the resource after a failure.


### -field ClusterResourceRestartNoNotify

Restart the resource after a failure. If the resource exceeds its restart threshold within its restart 
       period, do not attempt to <a href="https://msdn.microsoft.com/6722d075-02e0-4817-abc3-dce8951c17da">failover</a> the 
       <a href="https://msdn.microsoft.com/1e0680ba-87d0-4bf0-808c-d80485e4daa3">group</a> to another 
       <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> in the 
       <a href="c_gly.htm">cluster</a>.


### -field ClusterResourceRestartNotify

Restart the resource after a failure. If the resource exceeds its restart threshold within its restart 
       period, attempt to fail over the group to another node in the cluster. This is the default setting.


### -field ClusterResourceRestartActionCount

Defines the maximum value of the 
       <a href="https://msdn.microsoft.com/6300bdb7-2349-44f8-913a-dd84813bd3bd">CLUSTER_RESOURCE_RESTART_ACTION</a> enumeration.  It is not a valid value for the 
       <a href="https://msdn.microsoft.com/88be809b-a338-490a-82f3-886bfc2e3f37">RestartAction</a> property.


## -see-also




<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>



<a href="https://msdn.microsoft.com/88be809b-a338-490a-82f3-886bfc2e3f37">RestartAction</a>



<a href="https://msdn.microsoft.com/b84fe8fe-a49e-4c3c-acbd-f9cfe5ac0782">resource common property</a>
 

 

