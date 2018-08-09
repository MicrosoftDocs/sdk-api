---
UID: NF:msclus.ISClusNetInterface.get_State
title: ISClusNetInterface::get_State
author: windows-sdk-content
description: State of a network interface.
old-location: mscs\clusnetinterface_state.htm
old-project: mscs
ms.assetid: 3bc6bec3-bfe4-4ab4-8ad3-c42eba6d7cba
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ClusNetInterface object [Failover Cluster],State property, ClusNetInterface.State, ClusterNetInterfaceFailed, ClusterNetInterfaceStateUnknown, ClusterNetInterfaceUnavailable, ClusterNetInterfaceUnreachable, ClusterNetInterfaceUp, ISClusNetInterface.get_State, ISClusNetInterface::get_State, State property [Failover Cluster], State property [Failover Cluster],ClusNetInterface object, _wolf_clusnetinterface.state, get_State, mscs.clusnetinterface_state
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msclus.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MsClus.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: MsClus.tlb
tech.root: 
req.typenames: CLUS_GROUP_START_SETTING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsClus.dll
api_name:
 - ClusNetInterface.State
 - ISClusNetInterface.get_State
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusNetInterface::get_State


## -description


<p class="CCE_Message">[The <b>State</b> property 
    is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable 
    in subsequent versions.]

Returns information about 
    the state of a 
     <a href="https://msdn.microsoft.com/cc0cbbc3-e342-483e-9c94-4ee43f4d588d">network interface</a>.

This property is read-only.


## -parameters


## -remarks



For information on making constants defined by the Cluster Automation Server type library (MsClus.tlb) 
    available to scripts, see 
    <a href="https://msdn.microsoft.com/2ca508c9-c34a-4af5-a6c0-3d710171f3df">Creating a Cluster Automation Server Script</a>.




## -see-also




<a href="https://msdn.microsoft.com/8b4dc26c-0bac-4ff1-b5ae-4524c81ccdf7">CLUSTER_NETINTERFACE_STATE</a>



<a href="https://msdn.microsoft.com/21aaf37d-5b60-4005-9e7f-f0435de590b2">ClusNetInterface</a>



<a href="https://msdn.microsoft.com/d84a5e3f-d0f9-4345-b008-e15c277dcbd5">GetClusterNetInterfaceState</a>
 

 

