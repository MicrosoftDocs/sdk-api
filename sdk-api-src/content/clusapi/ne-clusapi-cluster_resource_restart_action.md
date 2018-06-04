---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
       <a href="https://msdn.microsoft.com/library/windows/hardware/dn934674">group</a> to another 
       <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> in the 
       <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a>.


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
 

 

