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

# __MIDL___MIDL_itf_msclus_0000_0000_0001 enumeration


## -description


Specifies the type of cluster group to create.


## -enum-fields




### -field ClusGroupTypeCoreCluster

A core cluster group.


### -field ClusGroupTypeAvailableStorage

An available storage cluster group.


### -field ClusGroupTypeTemporary

A temporary cluster group.


### -field ClusGroupTypeSharedVolume

A shared volume.


### -field ClusGroupTypeStoragePool

A storage pool.


### -field ClusGroupTypeFileServer

A file server.


### -field ClusGroupTypePrintServer

A print server.


### -field ClusGroupTypeDhcpServer

A Dynamic Host Configuration Protocol (DHCP) server.


### -field ClusGroupTypeDtc

A Distributed Transaction Coordinator (DTC) service.


### -field ClusGroupTypeMsmq

An Microsoft Message Queuing (MSMQ) service.


### -field ClusGroupTypeWins

A Windows Internet Name Service (WINS).


### -field ClusGroupTypeStandAloneDfs

A standalone Distributed File System (DFS).


### -field ClusGroupTypeGenericApplication

A generic application.


### -field ClusGroupTypeGenericService

A generic service.


### -field ClusGroupTypeGenericScript

A generic script.


### -field ClusGroupTypeIScsiNameService

An  Internet Small Computer System Interface (iSCSI) name service.


### -field ClusGroupTypeVirtualMachine

A virtual machine.


### -field ClusGroupTypeTsSessionBroker

A Terminal Services  Session  Broker.


### -field ClusGroupTypeIScsiTarget

An iSCSI target.


### -field ClusGroupTypeScaleoutFileServer

A Scale-Out File Server.


### -field ClusGroupTypeVMReplicaBroker

A virtual machine  replica broker.


### -field ClusGroupTypeTaskScheduler

A task scheduler.


### -field ClusGroupTypeClusterUpdateAgent

A cluster update agent.


### -field ClusGroupTypeScaleoutCluster

A cluster on a scale-out file server.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This member is not supported until Windows Server 2016.


### -field ClusGroupTypeStorageReplica

A storage replica.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This member is not supported until Windows Server 2016.


### -field ClusGroupTypeVMReplicaCoordinator

A virtual machine replica coordinator.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This member is not supported until Windows Server 2016.


### -field ClusGroupTypeCrossClusterOrchestrator

A cross-cluster orchestrator.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This member is not supported until Windows Server 2016.


### -field ClusGroupTypeInfrastructureFileServer


### -field ClusGroupTypeUnknown

An unknown cluster group type.


## -see-also




<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>
 

 

